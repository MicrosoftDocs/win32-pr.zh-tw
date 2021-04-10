---
title: 'MM_ACM_FILTERCHOOSE 訊息 (Msacm.imaadpcm .h) '
description: MM 的 \_ \_ FILTERCHOOSE 訊息會在將專案新增至三個下拉式清單方塊的其中一個之前，通知 acmFilterChoose 對話方塊攔截函式。
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- MM_ACM_FILTERCHOOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093987"
---
# <a name="mm_acm_filterchoose-message"></a>MM \_ 的 \_ FILTERCHOOSE 訊息

**MM 的 \_ \_ FILTERCHOOSE** 訊息會在將專案新增至三個下拉式清單方塊的其中一個之前，通知 [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose)對話方塊攔截函式。 此訊息可讓應用程式進一步自訂透過使用者介面所提供的選項。


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

要初始化的下拉式清單方塊，以及驗證或加入作業。



| 需求 | 值 |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FILTERCHOOSE \_ 自訂 \_ 驗證    | *LParam* 參數是要加入至 [自訂名稱] 下拉式清單方塊之 [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter)結構的指標。                                                                                                   |
| FILTERCHOOSE \_ 篩選準則 \_ 新增       | *LParam* 參數是緩衝區的指標，會接受要加入至 [篩選] 下拉式清單方塊中的 [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter)結構。 應用程式必須複製要加入至此緩衝區的篩選結構。 |
| FILTERCHOOSE \_ 篩選準則 \_ 驗證    | *LParam* 參數是要加入至 [篩選] 下拉式清單方塊之 [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter)結構的指標。                                                                                                        |
| FILTERCHOOSE \_ FILTERTAG \_ 新增    | *LParam* 參數是 **DWORD** 的指標，會接受要加入 [篩選標記] 下拉式清單方塊中的波形音訊篩選標記。                                                                                        |
| FILTERCHOOSE \_ FILTERTAG \_ 驗證 | *LParam* 參數是要列在 [篩選標記] 下拉式清單方塊中的波形音訊篩選標記。                                                                                                                                 |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

**WParam** 參數中指定的清單方塊所定義的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果應用程式處理 FILTERCHOOSE \_ 篩選 \_ 新增作業，則 *lParam* 中提供的記憶體緩衝區大小將會從 [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) 函式決定。

如果應用程式處理驗證作業，應用程式必須在傳回值之前加上 **SetWindowLong** (HWND，DWL \_ MSGRESULT， (LONG) **FALSE**) 以防止對話方塊列出此選取專案或 **SetWindowLong** (hwnd、DWL \_ MSGRESULT、 (LONG) **TRUE**) ，讓對話方塊可以列出此選取專案。 如果處理新增作業，應用程式必須在 **SetWindowLong** (HWND，DWL \_ MSGRESULT， (LONG) **FALSE**) 以表示不需要再新增，或使用 **SetWindowLong** (hwnd，DWL \_ MSGRESULT， (long) **TRUE**) 如果需要更多新增專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Msacm.imaadpcm。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[音訊壓縮管理員](audio-compression-manager.md)
</dt> <dt>

[音訊壓縮訊息](audio-compression-messages.md)
</dt> </dl>

 

 





