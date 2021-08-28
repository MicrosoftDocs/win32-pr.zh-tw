---
description: 指定和設定在呼叫 CoCreateActivity 或 CoEnterServiceDomain 時所輸入的服務網域中要使用的服務。
ms.assetid: f546ded4-255e-4565-b588-f36175902778
title: 'CServiceConfig 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CServiceConfig
api_type:
- COM
ms.openlocfilehash: a72a7c05317973813b5f19a9e486f3effe8f052547caa54314aad92079ffa0a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954208"
---
# <a name="cserviceconfig-class"></a>CServiceConfig 類別

指定和設定在呼叫 [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) 或 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)時所輸入的服務網域中要使用的服務。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID \_ CServiceConfig                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ProgID     | L "COMSVCS。CServiceConfig"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 介面 | [**IServiceComTIIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [**IServiceIISIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [**IServiceInheritanceConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [**IServicePartitionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [**IServiceSxSConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [**IServiceSynchronizationConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [**IServiceThreadPoolConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [**IServiceTrackerConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [**IServiceTransactionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## <a name="when-to-use"></a>使用時機

使用這個類別來設定您想要使用的服務。 [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) 和 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) 可讓您使用此類別所設定的服務，而不需要先將這些服務系結至元件，再加以使用。

此類別不是設計用來 Visual Basic。

## <a name="remarks"></a>備註

若要建立這個物件，請呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。

從 **CServiceConfig** 類別具現化的物件會匯總無限制執行緒封送處理器，使其可由系統執行時間儲存並重複使用於不同的單元中。

若要設定個別服務，請呼叫與服務相關聯之介面的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後呼叫該介面上的方法來建立適當的設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP （含 SP1） \[ 桌面應用程式\]<br/>                                 |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>ComSvcs。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[**CoCreateFreeThreadedMarshaler**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)
</dt> <dt>

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[沒有元件的 COM + 服務](com--services-without-components.md)
</dt> </dl>

 

