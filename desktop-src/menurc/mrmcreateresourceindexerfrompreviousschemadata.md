---
title: 'MrmCreateResourceIndexerFromPreviousSchemaData 函式 (MrmResourceIndexer) '
description: 從先前對 MrmDumpPriFileInMemory 或 MrmDumpPriDataInMemory 的呼叫所建立的記憶體內部架構資料，建立資源索引子。
ms.assetid: D9C90C12-CEFE-4794-9553-8BFBE9E43D99
keywords:
- MrmCreateResourceIndexerFromPreviousSchemaData 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621500f8f35714daad0e259e6a718c25129987dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465600"
---
# <a name="mrmcreateresourceindexerfrompreviousschemadata-function"></a>MrmCreateResourceIndexerFromPreviousSchemaData 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

從先前對 [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) 或 [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)的呼叫所建立的記憶體內部架構資料，建立資源索引子。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。

## <a name="syntax"></a>語法


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaData(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *schemaXmlData,
  _In_     ULONG                    schemaXmlSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*projectRoot* \[在\]
</dt> <dd>

類型： **PCWSTR**

您將產生 PRI 檔案之 UWP 應用程式的專案根目錄。 換句話說，是該應用程式資源檔的路徑。 您可以指定此項，如此您就可以在對相同資源索引子的後續 API 呼叫中，指定相對於該根目錄的路徑。

</dd> <dt>

*platformVersion* \[在\]
</dt> <dd>

類型： **[ **MrmPlatformVersion**](mrmplatformversion.md)**

資源索引子的目標平臺版本。

</dd> <dt>

*defaultQualifiers* \[在中，選擇性\]
</dt> <dd>

類型： **PCWSTR**

預設資源限定詞的清單。 例如，L "language-en-us \_ scale-100 \_ 對比-標準"

</dd> <dt>

*schemaXmlData* \[在\]
</dt> <dd>

類型： **BYTE \** _

先前呼叫 [_ *MrmDumpPriFileInMemory* *](mrmdumpprifileinmemory.md)或 [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)所建立之架構資料的指標。 在您完成使用此函數所建立的資源索引子之前，請勿釋放 *schemaXmlData* 。

</dd> <dt>

*schemaXmlSize* \[在\]
</dt> <dd>

類型： **ULONG**

*SchemaXmlData* 所指向之資料的大小。

</dd> <dt>

*索引子* \[in、out\]
</dt> <dd>

類型： **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _

資源索引子控制碼的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

如果函式 \_ 成功，則為 [正常]，否則為其他值。 使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。

## <a name="remarks"></a>備註

在您完成使用此函數所建立的資源索引子之前，請勿釋放 *schemaXmlData* 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1803版桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | \[僅限 Windows Server desktop 應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>MrmResourceIndexer。h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Mrmsupport .lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[套件資源索引 (PRI) API 和自訂建置系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

