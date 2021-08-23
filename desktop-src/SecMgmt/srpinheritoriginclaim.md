---
description: 此函式會採用原始屬性（如果原始權杖中有提供），並在繼承權杖的複本上設定這些屬性，並傳回重複的標記。
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: srpInheritOriginClaim 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 64436c699f5cb24b2a12675342078242a340fb2e53de3a6a8f3224d8b88beac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004884"
---
# <a name="srpinheritoriginclaim-function"></a>srpInheritOriginClaim 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

此函式會採用原始屬性（如果原始權杖中有提供），並在繼承權杖的複本上設定這些屬性，並傳回重複的標記。 然後，呼叫端可以模擬傳回的權杖。 此函數沒有相關聯的匯入程式庫。 您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 srpapi.dll。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OriginToken* \[在\]
</dt> <dd>

權杖的控制碼，這個標記會重複，並接收繼承的原始屬性。 這個控制碼必須以權杖 \_ 重複存取權限開啟。

</dd> <dt>

*InheritingToken* \[在\]
</dt> <dd>

權杖的控制碼，這個標記會重複，並接收繼承的原始屬性。 這個控制碼必須以權杖 \_ 重複存取權限開啟。 

</dd> <dt>

*ResultToken* 
</dt> <dd>

成功時，接收重複的標記。 呼叫端可以模擬它，以使用繼承的原始屬性來執行作業。 呼叫端會取得此控制碼的擁有權，而且必須將其關閉。 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Srpapi.dll</dt> </dl> |



 

