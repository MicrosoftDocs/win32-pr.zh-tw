---
title: 'MrmPeekResourceIndexerMessages 函式 (MrmResourceIndexer) '
description: 查看資源索引子所產生的任何訊息。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: 87D093AE-7444-4778-8B9E-1D0D972C90E1
keywords:
- MrmPeekResourceIndexerMessages 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmPeekResourceIndexerMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f72325ab147656873af2bbf13d7ce1cfa47802c816dc9f14f0c6ee4f3c821683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847328"
---
# <a name="mrmpeekresourceindexermessages-function"></a>MrmPeekResourceIndexerMessages 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

查看資源索引子所產生的任何訊息。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。

## <a name="syntax"></a>語法


```C++
HRESULT HRESULT MrmPeekResourceIndexerMessages(
  _In_  MrmResourceIndexerHandle  indexer,
  _Out_ MrmResourceIndexerMessage **messages,
  _Out_ ULONG                     *numMsgs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引子* \[在\]
</dt> <dd>

類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

識別您想要查看之訊息的資源索引子的控制碼。

</dd> <dt>

*訊息* \[擴展\]
</dt> <dd>

類型： **[ **MrmResourceIndexerMessage**](mrmresourceindexermessage.md)\*\***

指向 [**MrmResourceIndexerMessage**](mrmresourceindexermessage.md)指標的指標。 函數會配置 **MrmResourceIndexerMessage** 的陣列，並將指標傳回 *訊息* 中的該記憶體。 請勿釋放您傳遞給 *訊息* 的位址指標。

</dd> <dt>

*numMsgs* \[擴展\]
</dt> <dd>

類型： **ULONG \***

*訊息* 中傳回的訊息數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式 \_ 成功，則為 [正常]，否則為其他值。 使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。

## <a name="remarks"></a>備註

您的應用程式不會擁有在 *訊息* 中配置和傳回的記憶體，因此請勿釋放它。

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

 

