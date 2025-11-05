# lodash.com

The Lodash website.

## Running Locally

1. Clone the repository locally.

2. Ensure you are using the correct versions of both Ruby and Node:
    ```sh
    cd lodash.com

    # Install Node 11 (required for legacy Gulp build system)
    nvm install && nvm use # uses version from .nvmrc

    # Install Ruby 3.4+ via Homebrew
    brew install ruby

    # Add to your PATH (if not already done)
    echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
    source ~/.zshrc

    # Verify versions
    node --version  # Should show v11.x.x
    ruby --version  # Should show 3.4.x
    ```

3. Install required [gems](http://bundler.io/) & [packages](https://www.npmjs.com/) in the repository directory.
    ```shell
    $ bundle
    $ npm i
    ```

4. Build & run.
    ```shell
    $ bundle exec jekyll serve
    ```

## Incrementing the Lodash Version

1. Generate new documentation by running `npm run doc:sitehtml` from the [Lodash repository](https://github.com/lodash/lodash).

2. Copy the generated documentation from `lodash/doc/` to `lodash.com/docs/`.

3. Update `_config.yml` for the release.
    ```shell
    $ npm run build:config <version>
    ```
