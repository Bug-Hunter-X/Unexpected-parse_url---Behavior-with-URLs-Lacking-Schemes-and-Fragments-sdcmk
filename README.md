This repository demonstrates an uncommon bug in PHP's `parse_url()` function. The bug arises when parsing URLs that lack a scheme (e.g., 'http://', 'https://') but include a fragment identifier. In such cases, `parse_url()` may fail to correctly extract the fragment component, leading to unexpected results. This repository includes both the buggy code and a corrected version demonstrating how to handle these edge cases robustly.  The issue is particularly relevant when dealing with user-submitted URLs, where input validation is crucial. The solution utilizes regular expressions to ensure correct fragment extraction and handles cases where the scheme is missing. The detailed explanation can be found in the comments of the provided code files.