---
description: 設定專家 DLL 內的專家。
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: '設定回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 528e83c72b015bdac288b9e2c7e4838f665c92991f83c6f1eb105d454cb6ac74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064152"
---
# <a name="configure-callback-function"></a>設定回呼函數

設定函式會 **設定** 專家 DLL 內的專家。

專家必須實行 **設定** 函數。 收到函式呼叫時，專家會顯示一個對話方塊，讓使用者變更任何可設定的專案。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hExpertKey* \[在\]
</dt> <dd>

獨特的專家識別碼。

唯一的識別碼會傳回給所有專家特定的網路監視器函式。 請注意，此識別碼可能與傳遞給 [**Run**](run.md) 函式的識別碼不是相同的專家索引鍵。 請勿將專家金鑰儲存在 **設定** 呼叫中。

</dd> <dt>

*ppConfig* \[in、out\]
</dt> <dd>

進入時 [**EXPERTCONFIG**](expertconfig.md) 結構指標的指標。

成功結束之後，所參考的 [**EXPERTCONFIG**](expertconfig.md) 結構就會包含新的設定資料。

</dd> <dt>

*pExpertStartupInfo* \[在\]
</dt> <dd>

當專家開始時，具有焦點的 capture 元素指標。

</dd> <dt>

*StartupFlags* \[在\]
</dt> <dd>

指出專家應該如何使用 *pExpertStartupInfo* 參數的旗標。 唯一定義的旗標是「專家啟動」旗標，會 **\_ 在設定 \_ \_ \_ \_ \_ \_ \_ 資料上使用啟動資料**。 旗標表示專家將使用 *pExpertStartupInfo* 參數，而不是傳入的 *ppConfig* 參數。 一般來說，當您從操作功能表啟動專家時，會設定旗標。

</dd> <dt>

*hWnd* \[在\]
</dt> <dd>

父視窗的控制碼。 使用控制碼開啟對話方塊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (也就是，如果目前的設定存在) ，則傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

網路監視器會使用專家的目前設定來呼叫 **Configure** 函數（如果有的話）。 專家會顯示一個對話方塊，您可以在其中變更任何可設定的專案。

當傳入 *ppConfig* ，且網路監視器沒有為指定專家儲存的設定時，參數值可以是 **Null**。 在此情況下， **設定** 函數會假設 (或的硬式編碼預設值，會使用啟動資訊) 來開啟對話方塊。

設定函式傳回時，**設定** 資料也可以是 **null** ，而且傳入的是 **null** 。 當網路監視器沒有預存預設值，且使用者按下 [ **取消**] 時，就會發生這種情況。

[**EXPERTCONFIG**](expertconfig.md)資料結構的開頭包含儲存結構大小資訊的私用區段。 **EXPERTCONFIG** 結構的大小應該包含出現在結構開頭的保留 **DWORD** 長度。 例如，如果您的設定資料需要20個位元組的儲存空間，請配置24個位元組來儲存資料。 如果 *ppConfig* 為 **Null**，則 **Configure** 函式會呼叫 [**ExpertAllocMemory**](expertallocmemory.md) 函式，以配置大小正確的新設定。 如果緩衝區不足以保存專家資料，專家應該呼叫 [**ExpertReallocMemory**](expertreallocmemory.md) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




