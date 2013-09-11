# NAME

DBIx::Class::ResultSet::Excel - Excel export for DBIx::Class using Spreedsheet::WriteExcel

# SYNOPSIS

    package MyApp::Schema::ResultSet::Artist;
    use base 'DBIx::Class::ResultSet::Excel';

    1;

    use MyApp::Schema;
    my $schema = MyApp::Schema->connect($dbi_dsn, $user, $pass, \%dbi_params);

    # Query for all artists and put them in an array,
    # or retrieve them as a result set object.
    # $schema->resultset returns a DBIx::Class::ResultSet
    my ($fh, $filename) = $schema->resultset('Artist')->export_excel;

# DESCRIPTION

DBIx::Class::ResultSet::Excel is an extension of the Basic DBIx::Class::ResultSet with an extra function to export the ResultSet as an excel file.

# AUTHOR

Sean Zellmer <sean@lejeunerenard.com>
[http://www.lejeunenrenard.com](http://www.lejeunenrenard.com)

# COPYRIGHT

Copyright 2013- Sean Zellmer

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# DEPENDENCIES

The following modules are mandatory:

- [DBIx::Class](http://search.cpan.org/perldoc?DBIx::Class)
- [Spreadsheet::WriteExcel](http://search.cpan.org/perldoc?Spreadsheet::WriteExcel)
- [File::Temp](http://search.cpan.org/perldoc?File::Temp)
