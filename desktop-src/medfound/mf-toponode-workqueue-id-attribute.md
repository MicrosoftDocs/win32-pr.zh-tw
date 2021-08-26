---
description: 指定拓撲分支的工作佇列。
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: 'MF_TOPONODE_WORKQUEUE_ID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ba4ab55d2a70b4b0c081544ab43a78719fab537fbf478519bde1e65dfc9e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955088"
---
# <a name="mf_toponode_workqueue_id-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼屬性

指定拓撲分支的工作佇列。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。 屬性是選擇性的。

屬性的值是工作佇列的應用程式定義識別碼。

應用程式可以使用這個屬性，將工作佇列指派給拓撲的分支。 拓撲中的每個來源節點都會定義一個分支。 分支包含每個從該節點接收資料的拓撲節點。

如果設定此屬性，請在已解析的拓撲上呼叫 [**IMFWorkQueueServices：： BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) 方法。 拓撲中的多個分支可以共用相同的工作佇列，而工作佇列可以跨拓撲重複使用。

> [!Note]  
> 這個屬性的值與 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) 函數所傳回的識別碼不同。 屬性的值是應用程式定義的識別碼，可用來將拓撲分支與工作佇列產生關聯。 當媒體會話配置新的工作佇列時，它會在內部儲存實際的工作佇列識別碼。

 

如果設定此屬性，則應用程式也可以藉由設定 [ [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別**](mf-toponode-workqueue-mmcss-class-attribute.md) ] 屬性，將分支指派給多媒體類別排程器服務 (MMCSS) 工作。

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

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別**](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> <dt>

[工作佇列](work-queues.md)
</dt> </dl>

 

 




