## API Report File for "@backstage/backend-defaults"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { AwsCredentialsManager } from '@backstage/integration-aws-node';
import { AwsS3Integration } from '@backstage/integration';
import { AzureBlobStorageIntergation } from '@backstage/integration';
import { AzureCredentialsManager } from '@backstage/integration';
import { AzureDevOpsCredentialsProvider } from '@backstage/integration';
import { AzureIntegration } from '@backstage/integration';
import { BitbucketCloudIntegration } from '@backstage/integration';
import { BitbucketIntegration } from '@backstage/integration';
import { BitbucketServerIntegration } from '@backstage/integration';
import { GerritIntegration } from '@backstage/integration';
import { GiteaIntegration } from '@backstage/integration';
import { GithubCredentialsProvider } from '@backstage/integration';
import { GithubIntegration } from '@backstage/integration';
import { GitLabIntegration } from '@backstage/integration';
import { HarnessIntegration } from '@backstage/integration';
import { LoggerService } from '@backstage/backend-plugin-api';
import { Readable } from 'stream';
import { RootConfigService } from '@backstage/backend-plugin-api';
import { ServiceFactory } from '@backstage/backend-plugin-api';
import { ServiceRef } from '@backstage/backend-plugin-api';
import { UrlReaderService } from '@backstage/backend-plugin-api';
import { UrlReaderServiceReadTreeOptions } from '@backstage/backend-plugin-api';
import { UrlReaderServiceReadTreeResponse } from '@backstage/backend-plugin-api';
import { UrlReaderServiceReadUrlOptions } from '@backstage/backend-plugin-api';
import { UrlReaderServiceReadUrlResponse } from '@backstage/backend-plugin-api';
import { UrlReaderServiceSearchOptions } from '@backstage/backend-plugin-api';
import { UrlReaderServiceSearchResponse } from '@backstage/backend-plugin-api';

// @public
export class AwsS3UrlReader implements UrlReaderService {
  constructor(
    credsManager: AwsCredentialsManager,
    integration: AwsS3Integration,
    deps: {
      treeResponseFactory: ReadTreeResponseFactory;
    },
  );
  // (undocumented)
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(
    url: string,
    options?: UrlReaderServiceReadTreeOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(
    url: string,
    options?: UrlReaderServiceSearchOptions,
  ): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public
export class AzureBlobStorageUrlReader implements UrlReaderService {
  constructor(
    credsManager: AzureCredentialsManager,
    integration: AzureBlobStorageIntergation,
    deps: {
      treeResponseFactory: ReadTreeResponseFactory;
    },
  );
  // (undocumented)
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(
    url: string,
    options?: UrlReaderServiceReadTreeOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public
export class AzureUrlReader implements UrlReaderService {
  constructor(
    integration: AzureIntegration,
    deps: {
      treeResponseFactory: ReadTreeResponseFactory;
      credentialsProvider: AzureDevOpsCredentialsProvider;
    },
  );
  // (undocumented)
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(
    url: string,
    options?: UrlReaderServiceReadTreeOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(
    url: string,
    options?: UrlReaderServiceSearchOptions,
  ): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public
export class BitbucketCloudUrlReader implements UrlReaderService {
  constructor(
    integration: BitbucketCloudIntegration,
    deps: {
      treeResponseFactory: ReadTreeResponseFactory;
    },
  );
  // (undocumented)
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(
    url: string,
    options?: UrlReaderServiceReadTreeOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(
    url: string,
    options?: UrlReaderServiceSearchOptions,
  ): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public
export class BitbucketServerUrlReader implements UrlReaderService {
  constructor(
    integration: BitbucketServerIntegration,
    deps: {
      treeResponseFactory: ReadTreeResponseFactory;
    },
  );
  // (undocumented)
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(
    url: string,
    options?: UrlReaderServiceReadTreeOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(
    url: string,
    options?: UrlReaderServiceSearchOptions,
  ): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public @deprecated
export class BitbucketUrlReader implements UrlReaderService {
  constructor(
    integration: BitbucketIntegration,
    logger: LoggerService,
    deps: {
      treeResponseFactory: ReadTreeResponseFactory;
    },
  );
  // (undocumented)
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(
    url: string,
    options?: UrlReaderServiceReadTreeOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(
    url: string,
    options?: UrlReaderServiceSearchOptions,
  ): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public
export class FetchUrlReader implements UrlReaderService {
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(
    url: string,
    options?: UrlReaderServiceSearchOptions,
  ): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public
export type FromReadableArrayOptions = Array<{
  data: Readable;
  path: string;
  lastModifiedAt?: Date;
}>;

// @public
export class GerritUrlReader implements UrlReaderService {
  constructor(
    integration: GerritIntegration,
    deps: {
      treeResponseFactory: ReadTreeResponseFactory;
    },
  );
  // (undocumented)
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(
    url: string,
    options?: UrlReaderServiceReadTreeOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(
    url: string,
    options?: UrlReaderServiceSearchOptions,
  ): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public
export class GiteaUrlReader implements UrlReaderService {
  constructor(
    integration: GiteaIntegration,
    deps: {
      treeResponseFactory: ReadTreeResponseFactory;
    },
  );
  // (undocumented)
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(
    url: string,
    options?: UrlReaderServiceReadTreeOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(
    url: string,
    options?: UrlReaderServiceSearchOptions,
  ): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public
export class GithubUrlReader implements UrlReaderService {
  constructor(
    integration: GithubIntegration,
    deps: {
      treeResponseFactory: ReadTreeResponseFactory;
      credentialsProvider: GithubCredentialsProvider;
    },
  );
  // (undocumented)
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(
    url: string,
    options?: UrlReaderServiceReadTreeOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(
    url: string,
    options?: UrlReaderServiceSearchOptions,
  ): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public
export class GitlabUrlReader implements UrlReaderService {
  constructor(
    integration: GitLabIntegration,
    deps: {
      treeResponseFactory: ReadTreeResponseFactory;
    },
  );
  // (undocumented)
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(
    url: string,
    options?: UrlReaderServiceReadTreeOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(
    url: string,
    options?: UrlReaderServiceSearchOptions,
  ): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public
export class HarnessUrlReader implements UrlReaderService {
  constructor(
    integration: HarnessIntegration,
    deps: {
      treeResponseFactory: ReadTreeResponseFactory;
    },
  );
  // (undocumented)
  static factory: ReaderFactory;
  // (undocumented)
  read(url: string): Promise<Buffer>;
  // (undocumented)
  readTree(
    url: string,
    options?: UrlReaderServiceReadTreeOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  readUrl(
    url: string,
    options?: UrlReaderServiceReadUrlOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  // (undocumented)
  search(
    url: string,
    options?: UrlReaderServiceSearchOptions,
  ): Promise<UrlReaderServiceSearchResponse>;
  // (undocumented)
  toString(): string;
}

// @public
export type ReaderFactory = (options: {
  config: RootConfigService;
  logger: LoggerService;
  treeResponseFactory: ReadTreeResponseFactory;
}) => UrlReaderPredicateTuple[];

// @public
export interface ReadTreeResponseFactory {
  // (undocumented)
  fromReadableArray(
    options: FromReadableArrayOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  fromTarArchive(
    options: ReadTreeResponseFactoryOptions & {
      stripFirstDirectory?: boolean;
    },
  ): Promise<UrlReaderServiceReadTreeResponse>;
  // (undocumented)
  fromZipArchive(
    options: ReadTreeResponseFactoryOptions,
  ): Promise<UrlReaderServiceReadTreeResponse>;
}

// @public
export type ReadTreeResponseFactoryOptions =
  | {
      stream: Readable;
      subpath?: string;
      etag: string;
      filter?: (
        path: string,
        info?: {
          size: number;
        },
      ) => boolean;
    }
  | {
      response: Response;
      subpath?: string;
      etag?: string;
      filter?: (
        path: string,
        info?: {
          size: number;
        },
      ) => boolean;
    };

// @public
export class ReadUrlResponseFactory {
  static fromNodeJSReadable(
    oldStyleStream: NodeJS.ReadableStream,
    options?: ReadUrlResponseFactoryFromStreamOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  static fromReadable(
    stream: Readable,
    options?: ReadUrlResponseFactoryFromStreamOptions,
  ): Promise<UrlReaderServiceReadUrlResponse>;
  static fromResponse(
    response: Response,
  ): Promise<UrlReaderServiceReadUrlResponse>;
}

// @public
export type ReadUrlResponseFactoryFromStreamOptions = {
  etag?: string;
  lastModifiedAt?: Date;
};

// @public
export const urlReaderFactoriesServiceRef: ServiceRef<
  ReaderFactory,
  'plugin',
  'multiton'
>;

// @public
export type UrlReaderPredicateTuple = {
  predicate: (url: URL) => boolean;
  reader: UrlReaderService;
};

// @public
export class UrlReaders {
  static create(options: UrlReadersOptions): UrlReaderService;
  static default(options: UrlReadersOptions): UrlReaderService;
}

// @public
export const urlReaderServiceFactory: ServiceFactory<
  UrlReaderService,
  'plugin',
  'singleton'
>;

// @public
export type UrlReadersOptions = {
  config: RootConfigService;
  logger: LoggerService;
  factories?: ReaderFactory[];
};

// (No @packageDocumentation comment for this package)
```
