---
title: 'MrmCreateResourceFileInMemory 函式 (MrmResourceIndexer) '
description: 將 PRI 資訊建立為記憶體中的 blob，而不是磁片上的檔案。
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- MrmCreateResourceFileInMemory 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bbe36a55b5be18f9f4005b4e0ae24d3d610bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466597"
---
# <a name="mrmcreateresourcefileinmemory-function"></a>MrmCreateResourceFileInMemory 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

將 PRI 資訊建立為記憶體中的 blob，而不是磁片上的檔案。 此函式會配置記憶體，並將指標傳回至 *outputPriData* 中的該記憶體。 使用相同的指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) 來釋放該記憶體。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。

## <a name="syntax"></a>語法


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引子* \[在\]
</dt> <dd>

類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

識別資源索引子的控制碼，以從中建立 PRI 資訊。

</dd> <dt>

*packagingMode* \[在\]
</dt> <dd>

類型： **[ **MrmPackagingMode**](mrmpackagingmode.md)**

指定 PRI 資訊是否應獨立，或為資源套件。 不支援 **MrmPackagingModeAutoSplit** 。

</dd> <dt>

*packagingOptions* \[在\]
</dt> <dd>

類型： **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

指定 PRI 資訊的其他選項。

</dd> <dt>

*outputPriData* \[擴展\]
</dt> <dd>

類型：**位元組 \* \***

位元組指標的位址。 此函式會配置記憶體，並將指標傳回至 *outputPriData* 中的該記憶體。 使用您的位元組指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) ，以釋放該記憶體。

</dd> <dt>

*outputPriSize* \[擴展\]
</dt> <dd>

類型： **ULONG \** _

ULONG 的位址。 在 _outputPriSize * 中，此函式會傳回 *outputPriData* 所指向之已配置記憶體的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式 \_ 成功，則為 [正常]，否則為其他值。 使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。

## <a name="remarks"></a>備註

如果您將 *outputPriData* 傳遞至 [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md)，則在您完成使用資源索引子之前，請勿釋放記憶體。

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

 

