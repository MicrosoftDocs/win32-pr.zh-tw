---
description: 本檔包含 Windows 影像處理元件 (WIC) 定義的錯誤碼清單。
ms.assetid: 1ded909c-311b-49e3-ba23-b22cd7a77bc6
title: 編解碼器錯誤碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb8f3911516f11c4a0614461786d6f94eaf00e038e53babb47d4df595797bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207257"
---
# <a name="codec-error-codes"></a>編解碼器錯誤碼

本檔包含 Windows 影像處理元件 (WIC) 定義的錯誤碼清單。

-   [依程式碼的 WIC 錯誤](#wic-errors-by-code)
-   [依值的 WIC 錯誤](#wic-errors-by-value)

## <a name="wic-errors-by-code"></a>依程式碼的 WIC 錯誤

下表是 WICAPIs 依字母順序排序所使用的錯誤碼清單。 

| 錯誤碼                                      | 錯誤值                      |
|-------------------------------------------------|----------------------------------|
| WINCODEC \_ 錯誤已 \_ 中止                          | 0x80004004 (E \_ 中止)             |
| WINCODEC \_ ERR \_ ACCESSDENIED                     | 0x80070005 (E \_ ACCESSDENIED)      |
| WINCODEC \_ ERR \_ ALREADYLOCKED                    | 0x88982f0D                       |
| WINCODEC \_ ERR \_ BADHEADER                        | 0x88982f61                       |
| WINCODEC \_ ERR \_ BADIMAGE                         | 0x88982f60                       |
| WINCODEC \_ ERR \_ BADMETADATAHEADER                | 0x88982f63                       |
| WINCODEC \_ ERR \_ BADSTREAMDATA                    | 0x88982f70                       |
| WINCODEC \_ ERR \_ CODECNOTHUMBNAIL                 | 0x88982f44                       |
| WINCODEC \_ ERR \_ CODECPRESENT                     | 0x88982f43                       |
| WINCODEC \_ ERR \_ CODECTOOMANYSCANLINES            | 0x88982f46                       |
| WINCODEC \_ ERR \_ COMPONENTINITIALIZEFAILURE       | 0x88982f8B                       |
| WINCODEC \_ ERR \_ COMPONENTNOTFOUND                | 0x88982f50                       |
| WINCODEC \_ ERR \_ DUPLICATEMETADATAPRESENT         | 0x88982f8D                       |
| WINCODEC \_ ERR \_ FRAMEMISSING                     | 0x88982f62                       |
| WINCODEC \_ ERR \_ 泛型 \_ 錯誤                   | 0x80004005 (E \_) 失敗             |
| WINCODEC \_ ERR \_ IMAGESIZEOUTOFRANGE              | 0x88982f51                       |
| WINCODEC \_ ERR \_ INSUFFICIENTBUFFER               | 0x88982f8C                       |
| WINCODEC \_ ERR \_ INTERNALERROR                    | 0x88982f48                       |
| WINCODEC \_ ERR \_ INVALIDPARAMETER                 | 0x80070057 (E \_ INVALIDARG)        |
| WINCODEC \_ ERR \_ INVALIDQUERYCHARACTER            | 0x88982f93                       |
| WINCODEC \_ ERR \_ INVALIDQUERYREQUEST              | 0x88982f90                       |
| WINCODEC \_ ERR \_ INVALIDREGISTRATION              | 0x88982f8A                       |
| WINCODEC \_ ERR \_ NOTIMPLEMENTED                   | 0x80004001 (E \_ >notimpl)           |
| WINCODEC \_ ERR \_ NOTINITIALIZED                   | 0x88982f0C                       |
| WINCODEC \_ ERR \_ OUTOFMEMORY                      | 0x8007000E (E \_ OUTOFMEMORY)       |
| WINCODEC \_ ERR \_ PALETTEUNAVAILABLE               | 0x88982f45                       |
| WINCODEC \_ ERR \_ PROPERTYNOTFOUND                 | 0x88982f40                       |
| WINCODEC \_ ERR \_ PROPERTYNOTSUPPORTED             | 0x88982f41                       |
| WINCODEC \_ ERR \_ PROPERTYSIZE                     | 0x88982f42                       |
| WINCODEC \_ ERR \_ PROPERTYUNEXPECTEDTYPE           | 0x88982f8E                       |
| WINCODEC \_ ERR \_ REQUESTONLYVALIDATMETADATAROOT   | 0x88982f92                       |
| WINCODEC \_ ERR \_ SOURCERECTDOESNOTMATCHDIMENSIONS | 0x88982f49                       |
| WINCODEC \_ ERR \_ STREAMWRITE                      | 0x88982f71                       |
| WINCODEC \_ ERR \_ STREAMREAD                       | 0x88982f72                       |
| WINCODEC \_ ERR \_ STREAMNOTAVAILABLE               | 0x88982f73                       |
| WINCODEC \_ ERR \_ TOOMUCHMETADATA                  | 0x88982f52                       |
| WINCODEC \_ ERR \_ UNKNOWNIMAGEFORMAT               | 0x88982f07                       |
| WINCODEC \_ ERR \_ UNEXPECTEDMETADATATYPE           | 0x88982f91                       |
| WINCODEC \_ ERR \_ UNEXPECTEDSIZE                   | 0x88982f8F                       |
| WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION             | 0x88982f81                       |
| WINCODEC \_ ERR \_ UNSUPPORTEDPIXELFORMAT           | 0x88982f80                       |
| WINCODEC \_ ERR \_ UNSUPPORTEDVERSION               | 0x88982f0B                       |
| WINCODEC \_ ERR \_ VALUEOUTOFRANGE                  | 0x88982f05                       |
| WINCODEC \_ ERR \_ VALUEOVERFLOW                    | INTSAFE \_ E \_ 算術 \_ 溢位 |
| WINCODEC \_ ERR \_ WRONGSTATE                       | 0x88982f04                       |



 

## <a name="wic-errors-by-value"></a>依值的 WIC 錯誤

下表是 WICAPIs 依數位順序排序所使用的錯誤碼清單。 

| 錯誤碼                       | 錯誤值                                     |
|----------------------------------|-------------------------------------------------|
| 0x80004005 (E \_) 失敗             | WINCODEC \_ ERR \_ 泛型 \_ 錯誤                   |
| 0x80070057 (E \_ INVALIDARG)        | WINCODEC \_ ERR \_ INVALIDPARAMETER                 |
| 0x8007000E (E \_ OUTOFMEMORY)       | WINCODEC \_ ERR \_ OUTOFMEMORY                      |
| 0x80004001 (E \_ >notimpl)           | WINCODEC \_ ERR \_ NOTIMPLEMENTED                   |
| 0x80004004 (E \_ 中止)             | WINCODEC \_ 錯誤已 \_ 中止                          |
| 0x80070005 (E \_ ACCESSDENIED)      | WINCODEC \_ ERR \_ ACCESSDENIED                     |
| INTSAFE \_ E \_ 算術 \_ 溢位 | WINCODEC \_ ERR \_ VALUEOVERFLOW                    |
| 0x88982f04                       | WINCODEC \_ ERR \_ WRONGSTATE                       |
| 0x88982f05                       | WINCODEC \_ ERR \_ VALUEOUTOFRANGE                  |
| 0x88982f07                       | WINCODEC \_ ERR \_ UNKNOWNIMAGEFORMAT               |
| 0x88982f0B                       | WINCODEC \_ ERR \_ UNSUPPORTEDVERSION               |
| 0x88982f0C                       | WINCODEC \_ ERR \_ NOTINITIALIZED                   |
| 0x88982f0D                       | WINCODEC \_ ERR \_ ALREADYLOCKED                    |
| 0x88982f40                       | WINCODEC \_ ERR \_ PROPERTYNOTFOUND                 |
| 0x88982f41                       | WINCODEC \_ ERR \_ PROPERTYNOTSUPPORTED             |
| 0x88982f42                       | WINCODEC \_ ERR \_ PROPERTYSIZE                     |
| 0x88982f43                       | WINCODEC \_ ERR \_ CODECPRESENT                     |
| 0x88982f44                       | WINCODEC \_ ERR \_ CODECNOTHUMBNAIL                 |
| 0x88982f45                       | WINCODEC \_ ERR \_ PALETTEUNAVAILABLE               |
| 0x88982f46                       | WINCODEC \_ ERR \_ CODECTOOMANYSCANLINES            |
| 0x88982f48                       | WINCODEC \_ ERR \_ INTERNALERROR                    |
| 0x88982f49                       | WINCODEC \_ ERR \_ SOURCERECTDOESNOTMATCHDIMENSIONS |
| 0x88982f50                       | WINCODEC \_ ERR \_ COMPONENTNOTFOUND                |
| 0x88982f51                       | WINCODEC \_ ERR \_ IMAGESIZEOUTOFRANGE              |
| 0x88982f52                       | WINCODEC \_ ERR \_ TOOMUCHMETADATA                  |
| 0x88982f60                       | WINCODEC \_ ERR \_ BADIMAGE                         |
| 0x88982f61                       | WINCODEC \_ ERR \_ BADHEADER                        |
| 0x88982f62                       | WINCODEC \_ ERR \_ FRAMEMISSING                     |
| 0x88982f63                       | WINCODEC \_ ERR \_ BADMETADATAHEADER                |
| 0x88982f70                       | WINCODEC \_ ERR \_ BADSTREAMDATA                    |
| 0x88982f71                       | WINCODEC \_ ERR \_ STREAMWRITE                      |
| 0x88982f72                       | WINCODEC \_ ERR \_ STREAMREAD                       |
| 0x88982f73                       | WINCODEC \_ ERR \_ STREAMNOTAVAILABLE               |
| 0x88982f80                       | WINCODEC \_ ERR \_ UNSUPPORTEDPIXELFORMAT           |
| 0x88982f81                       | WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION             |
| 0x88982f8A                       | WINCODEC \_ ERR \_ INVALIDREGISTRATION              |
| 0x88982f8B                       | WINCODEC \_ ERR \_ COMPONENTINITIALIZEFAILURE       |
| 0x88982f8C                       | WINCODEC \_ ERR \_ INSUFFICIENTBUFFER               |
| 0x88982f8D                       | WINCODEC \_ ERR \_ DUPLICATEMETADATAPRESENT         |
| 0x88982f8E                       | WINCODEC \_ ERR \_ PROPERTYUNEXPECTEDTYPE           |
| 0x88982f8F                       | WINCODEC \_ ERR \_ UNEXPECTEDSIZE                   |
| 0x88982f90                       | WINCODEC \_ ERR \_ INVALIDQUERYREQUEST              |
| 0x88982f91                       | WINCODEC \_ ERR \_ UNEXPECTEDMETADATATYPE           |
| 0x88982f92                       | WINCODEC \_ ERR \_ REQUESTONLYVALIDATMETADATAROOT   |
| 0x88982f93                       | WINCODEC \_ ERR \_ INVALIDQUERYCHARACTER            |



 

 

 



