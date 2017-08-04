require 'html-proofer'
task :default => "test:htmlproof"

namespace :test do
  task :htmlproof do
    HTMLProofer.check_directory("./_site", {
        only_4xx: true,
        check_html: true,
        check_external_hash: true,
        disable_external: true,
        :cache => { :timeframe => '10h' },
        :typhoeus => { :ssl_verifyhost => 2, :timeout => 10 }
      }).run
  end
end
