# SwaggerClient-php
Flagr is a feature flagging, A/B testing and dynamic configuration microservice. The base path for all the APIs is \"/api/v1\".

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.1.12
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ConstraintApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\CreateConstraintRequest(); // \Swagger\Client\Model\CreateConstraintRequest | create a constraint
$flag_id = 789; // int | numeric ID of the flag
$segment_id = 789; // int | numeric ID of the segment

try {
    $result = $apiInstance->createConstraint($body, $flag_id, $segment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConstraintApi->createConstraint: ', $e->getMessage(), PHP_EOL;
}

$apiInstance = new Swagger\Client\Api\ConstraintApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$flag_id = 789; // int | numeric ID of the flag
$segment_id = 789; // int | numeric ID of the segment
$constraint_id = 789; // int | numeric ID of the constraint

try {
    $apiInstance->deleteConstraint($flag_id, $segment_id, $constraint_id);
} catch (Exception $e) {
    echo 'Exception when calling ConstraintApi->deleteConstraint: ', $e->getMessage(), PHP_EOL;
}

$apiInstance = new Swagger\Client\Api\ConstraintApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$flag_id = 789; // int | numeric ID of the flag
$segment_id = 789; // int | numeric ID of the segment

try {
    $result = $apiInstance->findConstraints($flag_id, $segment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConstraintApi->findConstraints: ', $e->getMessage(), PHP_EOL;
}

$apiInstance = new Swagger\Client\Api\ConstraintApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\CreateConstraintRequest(); // \Swagger\Client\Model\CreateConstraintRequest | create a constraint
$flag_id = 789; // int | numeric ID of the flag
$segment_id = 789; // int | numeric ID of the segment
$constraint_id = 789; // int | numeric ID of the constraint

try {
    $result = $apiInstance->putConstraint($body, $flag_id, $segment_id, $constraint_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConstraintApi->putConstraint: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to */api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ConstraintApi* | [**createConstraint**](docs/Api/ConstraintApi.md#createconstraint) | **POST** /flags/{flagID}/segments/{segmentID}/constraints | 
*ConstraintApi* | [**deleteConstraint**](docs/Api/ConstraintApi.md#deleteconstraint) | **DELETE** /flags/{flagID}/segments/{segmentID}/constraints/{constraintID} | 
*ConstraintApi* | [**findConstraints**](docs/Api/ConstraintApi.md#findconstraints) | **GET** /flags/{flagID}/segments/{segmentID}/constraints | 
*ConstraintApi* | [**putConstraint**](docs/Api/ConstraintApi.md#putconstraint) | **PUT** /flags/{flagID}/segments/{segmentID}/constraints/{constraintID} | 
*DistributionApi* | [**findDistributions**](docs/Api/DistributionApi.md#finddistributions) | **GET** /flags/{flagID}/segments/{segmentID}/distributions | 
*DistributionApi* | [**putDistributions**](docs/Api/DistributionApi.md#putdistributions) | **PUT** /flags/{flagID}/segments/{segmentID}/distributions | 
*EvaluationApi* | [**postEvaluation**](docs/Api/EvaluationApi.md#postevaluation) | **POST** /evaluation | 
*EvaluationApi* | [**postEvaluationBatch**](docs/Api/EvaluationApi.md#postevaluationbatch) | **POST** /evaluation/batch | 
*ExportApi* | [**getExportEvalCacheJSON**](docs/Api/ExportApi.md#getexportevalcachejson) | **GET** /export/eval_cache/json | 
*ExportApi* | [**getExportSqlite**](docs/Api/ExportApi.md#getexportsqlite) | **GET** /export/sqlite | 
*FlagApi* | [**createFlag**](docs/Api/FlagApi.md#createflag) | **POST** /flags | 
*FlagApi* | [**deleteFlag**](docs/Api/FlagApi.md#deleteflag) | **DELETE** /flags/{flagID} | 
*FlagApi* | [**findFlags**](docs/Api/FlagApi.md#findflags) | **GET** /flags | 
*FlagApi* | [**getFlag**](docs/Api/FlagApi.md#getflag) | **GET** /flags/{flagID} | 
*FlagApi* | [**getFlagEntityTypes**](docs/Api/FlagApi.md#getflagentitytypes) | **GET** /flags/entity_types | 
*FlagApi* | [**getFlagSnapshots**](docs/Api/FlagApi.md#getflagsnapshots) | **GET** /flags/{flagID}/snapshots | 
*FlagApi* | [**putFlag**](docs/Api/FlagApi.md#putflag) | **PUT** /flags/{flagID} | 
*FlagApi* | [**restoreFlag**](docs/Api/FlagApi.md#restoreflag) | **PUT** /flags/{flagID}/restore | 
*FlagApi* | [**setFlagEnabled**](docs/Api/FlagApi.md#setflagenabled) | **PUT** /flags/{flagID}/enabled | 
*HealthApi* | [**getHealth**](docs/Api/HealthApi.md#gethealth) | **GET** /health | 
*SegmentApi* | [**createSegment**](docs/Api/SegmentApi.md#createsegment) | **POST** /flags/{flagID}/segments | 
*SegmentApi* | [**deleteSegment**](docs/Api/SegmentApi.md#deletesegment) | **DELETE** /flags/{flagID}/segments/{segmentID} | 
*SegmentApi* | [**findSegments**](docs/Api/SegmentApi.md#findsegments) | **GET** /flags/{flagID}/segments | 
*SegmentApi* | [**putSegment**](docs/Api/SegmentApi.md#putsegment) | **PUT** /flags/{flagID}/segments/{segmentID} | 
*SegmentApi* | [**putSegmentsReorder**](docs/Api/SegmentApi.md#putsegmentsreorder) | **PUT** /flags/{flagID}/segments/reorder | 
*TagApi* | [**createTag**](docs/Api/TagApi.md#createtag) | **POST** /flags/{flagID}/tags | 
*TagApi* | [**deleteTag**](docs/Api/TagApi.md#deletetag) | **DELETE** /flags/{flagID}/tags/{tagID} | 
*TagApi* | [**findAllTags**](docs/Api/TagApi.md#findalltags) | **GET** /tags | 
*TagApi* | [**findTags**](docs/Api/TagApi.md#findtags) | **GET** /flags/{flagID}/tags | 
*VariantApi* | [**createVariant**](docs/Api/VariantApi.md#createvariant) | **POST** /flags/{flagID}/variants | 
*VariantApi* | [**deleteVariant**](docs/Api/VariantApi.md#deletevariant) | **DELETE** /flags/{flagID}/variants/{variantID} | 
*VariantApi* | [**findVariants**](docs/Api/VariantApi.md#findvariants) | **GET** /flags/{flagID}/variants | 
*VariantApi* | [**putVariant**](docs/Api/VariantApi.md#putvariant) | **PUT** /flags/{flagID}/variants/{variantID} | 

## Documentation For Models

 - [Constraint](docs/Model/Constraint.md)
 - [CreateConstraintRequest](docs/Model/CreateConstraintRequest.md)
 - [CreateFlagRequest](docs/Model/CreateFlagRequest.md)
 - [CreateSegmentRequest](docs/Model/CreateSegmentRequest.md)
 - [CreateTagRequest](docs/Model/CreateTagRequest.md)
 - [CreateVariantRequest](docs/Model/CreateVariantRequest.md)
 - [Distribution](docs/Model/Distribution.md)
 - [Error](docs/Model/Error.md)
 - [EvalContext](docs/Model/EvalContext.md)
 - [EvalDebugLog](docs/Model/EvalDebugLog.md)
 - [EvalResult](docs/Model/EvalResult.md)
 - [EvaluationBatchRequest](docs/Model/EvaluationBatchRequest.md)
 - [EvaluationBatchResponse](docs/Model/EvaluationBatchResponse.md)
 - [EvaluationEntity](docs/Model/EvaluationEntity.md)
 - [Flag](docs/Model/Flag.md)
 - [FlagSnapshot](docs/Model/FlagSnapshot.md)
 - [Health](docs/Model/Health.md)
 - [PutDistributionsRequest](docs/Model/PutDistributionsRequest.md)
 - [PutFlagRequest](docs/Model/PutFlagRequest.md)
 - [PutSegmentReorderRequest](docs/Model/PutSegmentReorderRequest.md)
 - [PutSegmentRequest](docs/Model/PutSegmentRequest.md)
 - [PutVariantRequest](docs/Model/PutVariantRequest.md)
 - [Segment](docs/Model/Segment.md)
 - [SegmentDebugLog](docs/Model/SegmentDebugLog.md)
 - [SetFlagEnabledRequest](docs/Model/SetFlagEnabledRequest.md)
 - [Tag](docs/Model/Tag.md)
 - [Variant](docs/Model/Variant.md)

## Documentation For Authorization

 All endpoints do not require authorization.


## Author



