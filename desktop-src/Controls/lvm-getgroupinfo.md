---
title: 'LVM_GETGROUPINFO 訊息 (Commctrl .h) '
description: 取得群組資訊。
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- LVM_GETGROUPINFO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5c48a21a1bba0c6dd1af3fd567ea853dc922591c553ea11a935fb705ad65bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411392"
---
# <a name="lvm_getgroupinfo-message"></a>LVM \_ GETGROUPINFO 訊息

取得群組資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>識別碼，指定要抓取其資訊的群組。</dd> <dt>

*lParam* 
</dt> <dd><a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a>結構的指標，此結構會接收抓取的資訊。 將此結構的 **cbSize** 成員設定為 SIZEOF (LVGROUP) 。 </dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回群組的識別碼，否則為-1。

## <a name="remarks"></a>備註

嘗試取得群組的標頭之前，請先確定群組沒有 LBGS \_ NOHEADER 樣式。

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





