---
title: 'LVM_MAPINDEXTOID 訊息 (Commctrl .h) '
description: 將專案的索引對應至唯一的識別碼。
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- LVM_MAPINDEXTOID message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a2a5de558b025e61bef26fd20278f125372769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464889"
---
# <a name="lvm_mapindextoid-message"></a>LVM \_ MAPINDEXTOID 訊息

將專案的索引對應至唯一的識別碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回唯一的識別碼。

## <a name="remarks"></a>備註

清單視圖控制項會依索引在內部追蹤專案。 這可能會造成問題，因為索引可能會在控制項的存留期間變更。

清單視圖控制項可以在建立專案時標記具有識別碼的專案。 您可以使用這個識別碼，在清單視圖控制項的存留期內保證唯一性。

若要唯一識別專案，請取得從呼叫傳回的索引，例如 [**IComponent：： GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) ，並呼叫 **LVM \_ MAPINDEXTOID**。 傳回值是唯一的識別碼。

> [!Note]  
> 在多執行緒環境中，只有裝載清單視圖控制項的執行緒（而不是背景執行緒）保證索引。

 

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

