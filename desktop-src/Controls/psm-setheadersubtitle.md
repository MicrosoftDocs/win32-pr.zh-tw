---
title: 'PSM_SETHEADERSUBTITLE 訊息 (Prsht.idl .h) '
description: 設定 wizard 內部頁面標頭的子標題文字。 您可以明確地傳送此訊息，或使用 PropSheet \_ SetHeaderSubTitle 宏。
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- PSM_SETHEADERSUBTITLE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934315"
---
# <a name="psm_setheadersubtitle-message"></a>PSM \_ SETHEADERSUBTITLE 訊息

設定 wizard 內部頁面標頭的子標題文字。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的 wizard 頁面索引。

</dd> <dt>

*lParam* 
</dt> <dd>

新的標頭副標題。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

如果您指定目前的頁面，則會立即重新繪製以顯示新的子標題。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl>      |
| Unicode 與 ANSI 名稱<br/>   | **PSM \_SETHEADERSUBTITLEW** (Unicode) 和 **PSM \_ SETHEADERSUBTITLEA** (ANSI) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**PSM \_ HWNDTOINDEX**](psm-hwndtoindex.md)
</dt> <dt>

[**PSM \_ IDTOINDEX**](psm-idtoindex.md)
</dt> <dt>

[**PSM \_ PAGETOINDEX**](psm-pagetoindex.md)
</dt> </dl>

 

 





