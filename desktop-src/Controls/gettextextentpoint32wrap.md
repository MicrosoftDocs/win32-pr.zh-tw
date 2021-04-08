---
title: GetTextExtentPoint32Wrap 函式
description: 計算指定文字字串的寬度和高度。 此函數會包裝對 GetTextExtentPoint 的呼叫。
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- GetTextExtentPoint32Wrap 函式 Windows 控制項
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685560"
---
# <a name="gettextextentpoint32wrap-function"></a>GetTextExtentPoint32Wrap 函式

\[**GetTextExtentPoint32Wrap** 可透過 Windows XP Service Pack 2 (SP2) 取得。 它可能會在後續版本中變更或無法使用。 建議您改為直接使用 [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) 。\]

計算指定文字字串的寬度和高度。 此函數會包裝對 [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa)的呼叫。

## <a name="syntax"></a>語法


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hdc* \[在\]
</dt> <dd>

類型： **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

裝置內容的控制碼。

</dd> <dt>

*lpString* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

包含要繪製之文字的緩衝區指標。 字串不需要以零結束，因為 *cbCount* 會指定字串的長度。

</dd> <dt>

*cbCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

*LpString* 所指向之字串的長度（以位元組為單位）。

</dd> <dt>

*lpSize* \[擴展\]
</dt> <dd>

類型： **LPSIZE**

當此方法傳回時，會包含 [**大小**](/previous-versions//dd145106(v=vs.85)) 結構的指標，其中包含字串的維度（以邏輯單位表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

如果成功，則傳回非零值;否則為0。

若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

**GetTextExtentPoint32Wrap** 不會依名稱匯出，也不會在公用標頭檔中宣告。 若要使用它，您必須從 ComCtl32.dll 使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數420來取得函式指標。

如需其他備註，請參閱 [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (5.81 版或更新版本) </dt> </dl> |



 

