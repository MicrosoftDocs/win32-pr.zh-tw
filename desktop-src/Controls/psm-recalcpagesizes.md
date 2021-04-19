---
title: 'PSM_RECALCPAGESIZES 訊息 (Prsht.idl .h) '
description: 新增或移除頁面之後，重新計算標準或 wizard 屬性工作表的頁面大小。 您可以明確地傳送此訊息，或使用 PropSheet \_ RecalcPageSizes 宏。
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- PSM_RECALCPAGESIZES message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969191"
---
# <a name="psm_recalcpagesizes-message"></a>PSM \_ RECALCPAGESIZES 訊息

新增或移除頁面之後，重新計算標準或 wizard 屬性工作表的頁面大小。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

建立屬性工作表時，它會調整大小以符合其初始的頁面集合。 為了維持與舊版通用控制項的相容性，屬性工作表和嚮導在後續新增或移除頁面時，不會自動調整大小。 使用通用控制項 [5.80 版](common-control-versions.md)時，應用程式應該在加入或移除具有 [**psm \_ ADDPAGE**](psm-addpage.md)、 [**psm \_ INSERTPAGE**](psm-insertpage.md)、 [**psm \_ REMOVEPAGE**](psm-removepage.md)或其對等宏的頁面之後傳送 **psm \_ RECALCPAGESIZES** 訊息。 它可確保屬性工作表的大小針對其目前的頁面集合正確調整大小。 如果未傳送此訊息，部分屬性工作表頁面可能會被截斷或太大。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





