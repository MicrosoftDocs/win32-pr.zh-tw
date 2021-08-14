---
description: 指定 MMCSS 拓撲分支的多媒體類別排程器服務 () 工作識別碼。
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: 'MF_TOPONODE_WORKQUEUE_MMCSS_TASKID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf75dc911c9d00cab2d21d937ef16a43b38cc4271299c6fae4f2ed7381ec63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739626"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID 屬性

指定 MMCSS 拓撲分支的多媒體類別排程器服務 () 工作識別碼。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。 此屬性是選擇性的。

除非也設定了下列屬性，否則會忽略此屬性：

-   [**MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼**](mf-toponode-workqueue-id-attribute.md)
-   [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別**](mf-toponode-workqueue-mmcss-class-attribute.md)

如果應用程式使用 MMCSS 註冊它自己的其中一個執行緒，您可以使用這個屬性來建立拓撲工作佇列與應用程式 MMCSS 群組的關聯。 將屬性值設定為等於當應用程式向 MMCSS 註冊時所收到的工作識別碼。  (在 [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa)函數的 *TaskIndex* 參數中傳回工作識別碼。 如需詳細資訊，請參閱主題 [進程和執行緒函數](../procthread/process-and-thread-functions.md)。 ) 

如果您想要讓 MMCSS 指派拓撲的新工作識別碼，請設定 [**mf \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別**](mf-toponode-workqueue-mmcss-class-attribute.md) 屬性，但不要設定 **mf \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID** 屬性。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> <dt>

[工作佇列](work-queues.md)
</dt> </dl>

 

 
