---
description: 指定拓撲分支的相對執行緒優先順序。
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: 'MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0667c91054f8711b8825cf421a2ee565b9161f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114020"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ PRIORITY 屬性

指定拓撲分支的相對執行緒優先順序。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。 屬性是選擇性的。

此屬性需要相同節點上的 [mf \_ TOPONODE \_ WORKQUEUE \_ 識別碼](mf-toponode-workqueue-id-attribute.md) 和 [mf \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別](mf-toponode-workqueue-mmcss-class-attribute.md) 屬性。

屬性的值是此拓撲分支之工作佇列的相對執行緒優先順序。 [多媒體類別](../procthread/multimedia-class-scheduler-service.md)排程器服務 (MMCSS) 會在設定執行緒優先順序時使用相對優先權。 如需詳細資訊，請參閱 [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority)。

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
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
