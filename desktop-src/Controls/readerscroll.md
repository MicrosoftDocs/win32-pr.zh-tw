---
title: ReaderScroll 回呼函式
description: 應用程式定義的回呼函式，當滑鼠指標在已宣告為使用中捲動區域的讀取器強制回應視窗部分內移動時，就會使用這個函數。
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- ReaderScroll 回呼函式 Windows 控制項
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934313"
---
# <a name="readerscroll-callback-function"></a>ReaderScroll 回呼函式

\[*ReaderScroll* 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

應用程式定義的回呼函式，當滑鼠指標在已宣告為使用中捲動區域的讀取器強制回應視窗部分內移動時，就會使用這個函數。

## <a name="syntax"></a>語法


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*prmi* \[在\]
</dt> <dd>

類型： **PREADERMODEINFO**

傳遞給 [**DoReaderMode**](doreadermode.md)函數的 [**READERMODEINFO**](readermodeinfo.md)結構指標。 此結構會定義讀取器強制回應視窗和現用捲動區域。

</dd> <dt>

 \[ 中的 dx\]
</dt> <dd>

類型： **int**

水準滾動的距離。 如果在 \_ [**READERMODEINFO**](readermodeinfo.md) 結構中設定 RMF VERTICALONLY 旗標，則此值一律為0。

</dd> <dt>

*dy* \[在\]
</dt> <dd>

類型： **int**

要垂直捲動的距離。 如果在 \_ [**READERMODEINFO**](readermodeinfo.md) 結構中設定 RMF HORIZONTALONLY 旗標，則此值一律為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

此函數應該一律傳回 **TRUE**。

## <a name="remarks"></a>備註

當應用程式收到來自此函式的通知時，應用程式會負責以 *dx* 和 *dy* 參數所指定的方向來滾動讀取器強制回應視窗。

## <a name="examples"></a>範例

下列範例概述使用自訂函式完成滾動的函式執行。


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows Vista \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>          |



 

