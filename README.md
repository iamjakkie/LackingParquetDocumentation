# LackingParquetDocumentation

This project will provide a basic documentation for older parquet/api, since the arrow project is one of the messiest thing I've worked with so far and I couldn't find any reliable docs, examples etc how to omit the arrow itself while reading parquet files.
The main reason for that is some misunderstanding in the Arrow/Parquet community - Arrow is an in-memory solution and parquet is a storage designed for big data. I have no idea how someone came to the conclusion that these two should be merged and people should start reading hundreds of gigs parquet files into memory.

According to Apache Arrow's statements if the data you're dealing with is too big to be fit into memory you should use partition. Cool, but how to re-partition the existing parquet files? You most probably would have to setup a spark cluster. 

I strongly believe there is a fundamental flaw with this design when you try to read the BIG DATA file format INTO MEMORY.

This repo will serve as a lower level parquet documentation.
