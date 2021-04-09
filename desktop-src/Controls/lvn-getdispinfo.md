---
title: 'LVN_GETDISPINFO (Commctrl 的通知碼) '
description: 由清單視圖控制項傳送至其父視窗。 它是父視窗的要求，可提供顯示或排序清單視圖專案所需的資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- LVN_GETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686679"
---
# <a name="lvn_getdispinfo-notification-code"></a>LVN \_ GETDISPINFO 通知碼

由清單視圖控制項傳送至其父視窗。 它是父視窗的要求，可提供顯示或排序清單視圖專案所需的資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)結構的指標。 在輸入時，此結構中所包含的 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構會指定所需的資訊類型，並識別感興趣的專案或子專案。 使用 **LVITEM** 結構，將要求的資訊傳回給控制項。 如果您的訊息處理常式 \_ \_ 在 **LVITEM** 結構的 **遮罩** 成員中設定 LVIF DI SETITEM 旗標，則清單視圖控制項會儲存要求的資訊，且不會再要求它。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

通知接收者會轉換 *lParam* 來取出 [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) 結構。 *WParam* 參數包含通知碼。

清單視圖控制項會傳送 **LVN \_ GETDISPINFO** 通知程式碼，以取得應用程式所儲存的專案資訊，而不是控制項。 此資訊可以是專案的文字或圖示資訊。 它也可以是專案狀態資訊。 請參閱 [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) 訊息，以取得以回呼為基礎執行專案狀態的詳細資訊。

如需清單視圖回呼的詳細資訊，請參閱 [回呼專案和回呼遮罩](list-view-controls-overview.md)。

## <a name="examples"></a>範例

下列範例顯示如何處理此通知程式碼，以在清單視圖的資料行中設定文字。 每個專案的資料會保存在下列結構中。


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



以下是來自于 \_ 對話方塊程式中的 WM 通知處理常式。


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVN \_GETDISPINFOW** (Unicode) 和 **LVN \_ GETDISPINFOA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LVN \_ SETDISPINFO**](lvn-setdispinfo.md)
</dt> </dl>

 

 





