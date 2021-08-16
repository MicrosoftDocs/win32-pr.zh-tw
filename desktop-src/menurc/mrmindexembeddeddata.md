---
title: 'MrmIndexEmbeddedData 函式 (MrmResourceIndexer) '
description: 編制屬於 UWP 應用程式的單一 embeddeddata 資源的索引。
ms.assetid: 4DA37CF9-43B6-44EE-8A10-DBD4510D7885
keywords:
- MrmIndexEmbeddedData 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmIndexEmbeddedData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7897df30506b66e74122c238e25a5b20fa5e1635e299c8a08db2519c842bdf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971997"
---
# <a name="mrmindexembeddeddata-function"></a>MrmIndexEmbeddedData 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

編制屬於 UWP 應用程式的單一 **embeddeddata** 資源的索引。 接受明確 (，但) 資源限定詞的選擇性清單。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。

## <a name="syntax"></a>語法


```C++
HRESULT HRESULT MrmIndexEmbeddedData(
  _In_           MrmResourceIndexerHandle indexer,
  _In_           PCWSTR                   resourceUri,
  _In_     const BYTE                     *embeddedData,
  _In_           ULONG                    embeddedDataSize,
  _In_opt_       PCWSTR                   qualifiers
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引子* \[在\]
</dt> <dd>

類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

識別將為資源檔編制索引之資源索引子的控制碼。

</dd> <dt>

*resourceUri* \[在\]
</dt> <dd>

類型： **PCWSTR**

要指派給資源的資源 URI。 當您稍後從此資源索引子產生 PRI 檔案時，會使用此路徑做為此資源的資源對應子樹名稱。

</dd> <dt>

*embeddedData* \[在\]
</dt> <dd>

類型： **CONST BYTE \***

您想要編制索引之資源的資料指標。

</dd> <dt>

*embeddedDataSize* \[在\]
</dt> <dd>

類型： **ULONG**

*EmbeddedData* 所指向之資料的大小。

</dd> <dt>

*限定詞* \[在中，選擇性\]
</dt> <dd>

類型： **PCWSTR**

選擇性的資源限定詞清單，例如 L "language-en-us \_ scale-100 \_ 對比-標準"。 空字串或 **nullptr** 表示中立的資源。 系統 *不* 會從 *resourceUri* 推斷資源限定詞。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式 \_ 成功，則為 [正常]，否則為其他值。 使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。

## <a name="remarks"></a>備註

如果您想要指定任何資源限定詞，請在 *限定詞* 參數中傳遞它們。 系統 *不* 會從 *resourceUri* 推斷資源限定詞。

使用 *resourceUri* 的檔案名區段做為資源名稱。

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

 

