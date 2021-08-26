---
title: 'MrmCreateConfigInMemory 函式 (MrmResourceIndexer) '
description: 建立新的初始化 PRI 設定資訊 (為記憶體內部資料，而不是檔案) 定義您指定的限定詞預設值。
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- MrmCreateConfigInMemory 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b30b4a64313952d48662a82e2f62cdef25106136e7757220668fc094c9258d4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011788"
---
# <a name="mrmcreateconfiginmemory-function"></a>MrmCreateConfigInMemory 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

建立新的初始化 PRI 設定資訊 (為記憶體內部資料，而不是檔案) 定義您指定的限定詞預設值。 此函式會配置記憶體，並將指標傳回至 *outputXmlData* 中的該記憶體。 使用相同的指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) 來釋放該記憶體。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。

## <a name="syntax"></a>語法


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*platformVersion* \[在\]
</dt> <dd>

類型： **[ **MrmPlatformVersion**](mrmplatformversion.md)**

平臺版本 (*targetOsVersion*) ，以用於產生的設定資訊。

</dd> <dt>

*defaultQualifiers* \[在中，選擇性\]
</dt> <dd>

類型： **PCWSTR**

預設資源限定詞的清單。 例如，L "language-en-us \_ scale-100 \_ 對比-標準"

</dd> <dt>

*outputXmlData* \[擴展\]
</dt> <dd>

類型：**位元組 \* \***

位元組指標的位址。 此函式會配置記憶體，並將指標傳回至 *outputXmlData* 中的該記憶體。 使用您的位元組指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) ，以釋放該記憶體。

</dd> <dt>

*outputXmlSize* \[擴展\]
</dt> <dd>

類型： **ULONG \***

ULONG 的位址。 在 *outputXmlSize* 中，此函式會傳回 *outputXmlData* 所指向之已配置記憶體的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式 \_ 成功，則為 [正常]，否則為其他值。 使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。

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

 

