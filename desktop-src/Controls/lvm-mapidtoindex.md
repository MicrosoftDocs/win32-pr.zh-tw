---
title: 'LVM_MAPIDTOINDEX 訊息 (Commctrl .h) '
description: 將專案的識別碼對應至索引。
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- LVM_MAPIDTOINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966136"
---
# <a name="lvm_mapidtoindex-message"></a>LVM \_ MAPIDTOINDEX 訊息

將專案的識別碼對應至索引。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

專案的唯一識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回最新的索引。

## <a name="remarks"></a>備註

清單視圖控制項會依索引在內部追蹤專案。 這可能會造成問題，因為索引可能會在控制項的存留期間變更。

清單視圖控制項可以在建立專案時標記具有識別碼的專案。 您可以使用這個識別碼，在清單視圖控制項的存留期內保證唯一性。

若要唯一識別專案，請取得從呼叫傳回的索引，例如 [**IComponent：： GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) ，並呼叫 [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md)。 傳回值是唯一的識別碼。

如果您在建立識別碼之後需要專案的索引，您可以使用唯一識別碼來呼叫 **LVM \_ MAPIDTOINDEX** ，它會傳回最新的索引。

**LVM \_** [**Lvs) \_ OWNERDATA**](list-view-window-styles.md)樣式下不支援 MAPIDTOINDEX。

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



 

