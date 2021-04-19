---
title: 'MrmDumpPriDataInMemory 函式 (MrmResourceIndexer) '
description: 傾印 PRI 資訊 (作為記憶體中的 blob，由先前對 MrmCreateResourceFileInMemory) 的呼叫所建立，以作為記憶體中資料) 的 XML 對等 (，以便更容易閱讀。
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- MrmDumpPriDataInMemory 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966142"
---
# <a name="mrmdumppridatainmemory-function"></a>MrmDumpPriDataInMemory 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

傾印 PRI 資訊 (作為記憶體中的 blob，由先前對 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) 的呼叫所建立，以作為記憶體中資料) 的 XML 對等 (，以便更容易閱讀。 此函式會配置記憶體，並將指標傳回至 *outputXmlData* 中的該記憶體。 使用相同的指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) 來釋放該記憶體。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。

## <a name="syntax"></a>語法


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*inputPriData* \[在\]
</dt> <dd>

類型： **BYTE \** _

對 [_ *MrmCreateResourceFileInMemory* *](mrmcreateresourcefileinmemory.md)之前的呼叫所建立之 PRI 資料的指標。

</dd> <dt>

*inputPriSize* \[在\]
</dt> <dd>

類型： **ULONG**

*InputPriData* 所指向之資料的大小。

</dd> <dt>

*schemaPriData* \[在中，選擇性\]
</dt> <dd>

類型： **BYTE \** _

PRI 資訊的選擇性指標 (作為記憶體中的 blob) 代表前一次呼叫 [_ *MrmCreateResourceFileInMemory* *](mrmcreateresourcefileinmemory.md)所建立的架構資料。 在您完成使用資源索引子之前，請勿釋放 *schemaPriData* 。 另請參閱備註。

</dd> <dt>

*schemaPriSize* \[在\]
</dt> <dd>

類型： **ULONG**

*SchemaPriData* 所指向之資料的大小。

</dd> <dt>

*dumpType* \[在\]
</dt> <dd>

類型： **[ **MrmDumpType**](mrmdumptype.md)**

指定 XML 傾印的詳細程度，或是否應該傾印架構。

</dd> <dt>

*outputXmlData* \[擴展\]
</dt> <dd>

類型：**位元組 \* \***

位元組指標的位址。 此函式會配置記憶體，並將指標傳回至 *outputXmlData* 中的該記憶體。 使用您的位元組指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) ，以釋放該記憶體。

</dd> <dt>

*outputXmlSize* \[擴展\]
</dt> <dd>

類型： **ULONG \** _

ULONG 的位址。 在 _outputXmlSize * 中，此函式會傳回 *outputXmlData* 所指向之已配置記憶體的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式 \_ 成功，則為 [正常]，否則為其他值。 使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。

## <a name="remarks"></a>備註

無架構的資源套件是使用傳遞至 [**MrmCreateResourceFile**](mrmcreateresourcefile.md)或 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (的 [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md)引數，或在 PRI 設定檔) 中使用 *omitSchemaFromResourcePacks* 參數所建立的資源套件。 若要傾印無架構的資源套件，請將主要封裝 PRI 資料的路徑傳遞為 *schemaPriData* 參數的引數。

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

 

