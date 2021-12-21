# longitude
Fostering topical discourse in the long term

## Method for Single Post

1. Start with URL

2. Determine if domain is a blog-hosting site (allow early exit)

    1. Ignore social media
    2. Ignore journals
    3. Ignore ads
    4. Ignore infrastructure/search engines
    5. Ignore commercial websites (company blogs)
    6. Single or multi-tenant hos

3. Determine if webpage is duplicate entry (allow early exit)

    1. Matching URL
    2. Matching domain
    3. Matching content

4. Passing above checks indicates that webpage is a blog

    1. Create entry in database

        1. Title
        2. Author
        3. Keywords
        4. Link
        5. Summary
        6. Domain (parent)
        7. References (relationship)
        8. Children (relationship)

5. Populate reference links by

    1. Parsing HTML for hrefs
    2. Drop all hrefs to same domain for single host, same blog for multi-host
    3. Drop hrefs to IGNORE domains
    4. Search remaining links to estimate value of links
    5. Limit to 5?

6. Check for child links by

    1. Query backlink service for specific URL
    2. Drop hrefs to same domain
    3. Drop hrefs to INGORE domains
    4. Search remaining links to estimate value of links
    5. Limit to 5?

7. Populate summary using text summarizer

    1. Quick summary for display during reference/child implementation
    2. Larger summary for display as center

8. Populate keywords using generator tool

## Method for Domain

1. Check blacklist (domains which do not fit use case)
2. Check single-tenant domains (already defined)
3. Check multi-tenant domains (already defined)
4. Create new domain object

    1. Root url for domain
    2. Root url for blog

#### Domain States

1. IGNORE
2. SINGLE
3. MULTI
4. POTENTIAL
