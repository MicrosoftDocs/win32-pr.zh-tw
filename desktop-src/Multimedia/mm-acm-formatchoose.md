---
title: 'MM_ACM_FORMATCHOOSE 訊息 (Msacm.imaadpcm .h) '
description: MM 的 \_ \_ FORMATCHOOSE 訊息會在將專案新增至三個下拉式清單方塊的其中一個之前，通知 acmFormatChoose 對話攔截函式。
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- MM_ACM_FORMATCHOOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686639"
---
# <a name="mm_acm_formatchoose-message"></a>MM \_ 的 \_ FORMATCHOOSE 訊息

**MM 的 \_ \_ FORMATCHOOSE** 訊息會在將專案新增至三個下拉式清單方塊的其中一個之前，通知 [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose)對話攔截函式。 此訊息可讓應用程式進一步自訂透過使用者介面所提供的選項。


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

要初始化的下拉式清單方塊，以及驗證或加入作業。



| 需求 | 值 |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATCHOOSE \_ 自訂 \_ 驗證    | *LParam* 參數是要加入至 [自訂名稱] 下拉式清單方塊之 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)結構的指標。                                                                                                   |
| \_新增 FORMATCHOOSE 格式 \_       | *LParam* 參數是緩衝區的指標，會接受要加入至 [格式] 下拉式清單方塊中的 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)結構。 應用程式必須複製要加入這個緩衝區的格式結構。 |
| FORMATCHOOSE \_ 格式 \_ 驗證    | *LParam* 參數是要加入至 [格式] 下拉式清單方塊之 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)結構的指標。                                                                                                        |
| FORMATCHOOSE \_ FORMATTAG \_ 新增    | *LParam* 參數是變數的指標，該變數會接受將波形音訊格式標記新增至 [格式標記] 下拉式清單方塊。                                                                                             |
| FORMATCHOOSE \_ FORMATTAG \_ 驗證 | *LParam* 參數是要在 [格式標記] 下拉式清單方塊中列出的波形音訊格式標記。                                                                                                                                     |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

**WParam** 參數中所指定清單方塊所定義的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果應用程式處理 FILTERCHOOSE \_ 格式的 \_ 新增作業， *lParam* 中提供的記憶體緩衝區大小將會從 [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) 函式決定。

如果您的應用程式正在處理驗證作業，它可以藉由呼叫 **SetWindowLong** 函數，並將 *NINDEX* 設定為 DWL \_ MSGRESULT，並將 *lNewLong* 設定為 **FALSE** (轉換為 **LONG** 資料類型) ，防止對話方塊列出此選取專案。 若要允許對話方塊列出此選項，請呼叫此函式，並將 *lNewLong* 設為 **TRUE**。

如果您的應用程式正在處理新增作業，它可能會藉由呼叫 **SetWindowLong** 函數，並將 *NINDEX* 設定為 DWL \_ MSGRESULT，並將 *lNewLong* 設定為 **FALSE** (轉換為 **LONG** 資料類型) ，來指出不再需要額外的新增作業。 若要指出需要更多新增專案，請呼叫此函式，並將 *lNewLong* 設為 **TRUE**。

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

 

