---
title: 'TTM_SETDELAYTIME 訊息 (Commctrl .h) '
description: 設定工具提示控制項的初始、彈出和 reshow 持續期間。
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- TTM_SETDELAYTIME message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934391"
---
# <a name="ttm_setdelaytime-message"></a>TTM \_ SETDELAYTIME 訊息

設定工具提示控制項的初始、彈出和 reshow 持續期間。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定要設定之時間值的旗標。 此參數可以是下列其中一個值



| 值                                                                                                                                                            | 意義                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**TTDT \_ AUTOPOP**</dt> </dl>       | 設定當指標在工具周框內為固定時，工具提示視窗保持可見的時間量。 若要將 autopop 延遲時間傳回為其預設值，請將 *lParam* 設定為-1。<br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ 初始**</dt> </dl>       | 設定在顯示工具提示視窗之前，指標必須保持在工具周框內保持靜止的時間量。 若要傳回初始延遲時間為其預設值，請將 *lParam* 設定為-1。<br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ RESHOW**</dt> </dl>          | 設定當指標從某個工具移至另一個工具時，後續工具提示視窗顯示所需的時間量。 若要將 reshow 延遲時間傳回為其預設值，請將 *lParam* 設定為-1。<br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <dt>**TTDT \_ 自動**</dt> </dl> | 將三個延遲時間設定為預設比例。 Autopop 時間將會是初始時間的10倍，而 reshow 時間會是最初的第一次。 如果設定此旗標，請使用正值 *lParam* 來指定初始時間（以毫秒為單位）。 將 *lParam* 設定為負值，以將所有三個延遲時間傳回至其預設值。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定延遲時間（以毫秒為單位）。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="remarks"></a>備註

預設的延遲時間是以按兩下時間為基礎。 針對500毫秒的預設按兩下時間，初始、autopop 和 reshow 延遲時間分別為500毫秒、5000毫秒和100毫秒。 下列程式碼片段會使用 [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) 函數來判斷任何系統的三個延遲時間。


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TTM \_ GETDELAYTIME**](ttm-getdelaytime.md)
</dt> </dl>

 

