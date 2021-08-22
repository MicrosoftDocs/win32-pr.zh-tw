---
title: 'MrmDumpPriFile 函式 (MrmResourceIndexer) '
description: 傾印 PRI 檔案 (這是其 XML 對等 (的二進位) ，以做為磁片) 上的檔案，以便更容易閱讀。
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- MrmDumpPriFile 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59e748f9ab41470ca85043f25b0116d17eb6877002891b5f5bba123cf06b2f40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119354768"
---
# <a name="mrmdumpprifile-function"></a>MrmDumpPriFile 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

傾印 PRI 檔案 (這是其 XML 對等 (的二進位) ，以做為磁片) 上的檔案，以便更容易閱讀。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。

## <a name="syntax"></a>語法


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*indexFileName* \[在\]
</dt> <dd>

類型： **PCWSTR**

PRI 檔案的完整檔案路徑。 這是將傾印至 XML 的 PRI 檔案。

</dd> <dt>

*schemaPriFile* \[在中，選擇性\]
</dt> <dd>

類型： **PCWSTR**

架構檔案的選擇性完整檔案路徑， (或代表架構的 PRI 檔案;請參閱備註) 。

</dd> <dt>

*dumpType* \[在\]
</dt> <dd>

類型： **[ **MrmDumpType**](mrmdumptype.md)**

指定 XML 傾印的詳細程度，或是否應該傾印架構。

</dd> <dt>

*outputXmlFile* \[在\]
</dt> <dd>

類型： **PCWSTR**

要建立的 XML 檔案的路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式 \_ 成功，則為 [正常]，否則為其他值。 使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。

## <a name="remarks"></a>備註

無架構的資源套件是使用傳遞至 [**MrmCreateResourceFile**](mrmcreateresourcefile.md)或 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (的 [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md)引數，或在 PRI 設定檔) 中使用 *omitSchemaFromResourcePacks* 參數所建立的資源套件。 若要傾印無架構的資源套件，請將主要封裝 PRI 資料的路徑傳遞為 *schemaPriFile* 參數的引數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1803版桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows\[僅限伺服器桌面應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>MrmResourceIndexer。h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Mrmsupport .lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[套件資源索引 (PRI) API 和自訂建置系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

