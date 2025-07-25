``w.consumer_listings``: Consumer Listings
==========================================
.. currentmodule:: databricks.sdk.service.marketplace

.. py:class:: ConsumerListingsAPI

    Listings are the core entities in the Marketplace. They represent the products that are available for
    consumption.

    .. py:method:: batch_get( [, ids: Optional[List[str]]]) -> BatchGetListingsResponse

        Batch get a published listing in the Databricks Marketplace that the consumer has access to.

        :param ids: List[str] (optional)

        :returns: :class:`BatchGetListingsResponse`
        

    .. py:method:: get(id: str) -> GetListingResponse

        Get a published listing in the Databricks Marketplace that the consumer has access to.

        :param id: str

        :returns: :class:`GetListingResponse`
        

    .. py:method:: list( [, assets: Optional[List[AssetType]], categories: Optional[List[Category]], is_free: Optional[bool], is_private_exchange: Optional[bool], is_staff_pick: Optional[bool], page_size: Optional[int], page_token: Optional[str], provider_ids: Optional[List[str]], tags: Optional[List[ListingTag]]]) -> Iterator[Listing]

        List all published listings in the Databricks Marketplace that the consumer has access to.

        :param assets: List[:class:`AssetType`] (optional)
          Matches any of the following asset types
        :param categories: List[:class:`Category`] (optional)
          Matches any of the following categories
        :param is_free: bool (optional)
          Filters each listing based on if it is free.
        :param is_private_exchange: bool (optional)
          Filters each listing based on if it is a private exchange.
        :param is_staff_pick: bool (optional)
          Filters each listing based on whether it is a staff pick.
        :param page_size: int (optional)
        :param page_token: str (optional)
        :param provider_ids: List[str] (optional)
          Matches any of the following provider ids
        :param tags: List[:class:`ListingTag`] (optional)
          Matches any of the following tags

        :returns: Iterator over :class:`Listing`
        

    .. py:method:: search(query: str [, assets: Optional[List[AssetType]], categories: Optional[List[Category]], is_free: Optional[bool], is_private_exchange: Optional[bool], page_size: Optional[int], page_token: Optional[str], provider_ids: Optional[List[str]]]) -> Iterator[Listing]

        Search published listings in the Databricks Marketplace that the consumer has access to. This query
        supports a variety of different search parameters and performs fuzzy matching.

        :param query: str
          Fuzzy matches query
        :param assets: List[:class:`AssetType`] (optional)
          Matches any of the following asset types
        :param categories: List[:class:`Category`] (optional)
          Matches any of the following categories
        :param is_free: bool (optional)
        :param is_private_exchange: bool (optional)
        :param page_size: int (optional)
        :param page_token: str (optional)
        :param provider_ids: List[str] (optional)
          Matches any of the following provider ids

        :returns: Iterator over :class:`Listing`
        