---
description: 指定拓撲分支的工作專案優先順序。
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: 'MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5f7df6630e41a32eeb069c2a07b8030da79929
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191626"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ 專案 \_ 優先順序屬性

指定拓撲分支的工作專案優先順序。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。 屬性是選擇性的。

此屬性需要相同節點上的 [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) 屬性。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> <dt>

[工作佇列和執行緒改進](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼**](mf-toponode-workqueue-id-attribute.md)
</dt> </dl>

 

 




