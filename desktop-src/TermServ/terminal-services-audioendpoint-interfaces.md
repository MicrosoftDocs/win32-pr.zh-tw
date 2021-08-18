---
title: 遠端桌面服務 AudioEndpoint 介面
description: 下列介面適用于 AudioEndpoint API。
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec12cd3d4648f3ed357e898f75850e77b3b679d59a92d9f0518f809ba52f58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000068"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a>遠端桌面服務 AudioEndpoint 介面

下列介面適用于 AudioEndpoint API。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

初始化裝置端點物件，並取得其所代表之裝置的功能。

</dd> <dt>

[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

提供有關音訊端點的音訊引擎資訊。 此介面是由音訊端點所執行。

</dd> <dt>

[**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

控制端點的資料流程狀態。

</dd> <dt>

[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

取得端點緩衝區中目前讀取和寫入位置之間的差異。

</dd> <dt>

[**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

取得每個處理階段的輸入緩衝區。

</dd> <dt>

[**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

取得每個處理階段的輸出緩衝區。

</dd> </dl>

## <a name="remarks"></a>備註

遠端桌面服務 AudioEndpoint API 適用于遠端桌面案例;它不適用於用戶端應用程式。

 

 




