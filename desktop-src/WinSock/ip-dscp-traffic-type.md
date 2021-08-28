---
description: 下表說明 IP \_ DSCP \_ 流量 \_ 類型通訊端選項。
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 87915dc214b0ba306b4f38dbd833b27199277564fa8c2815b9147e0d82253589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097848"
---
# <a name="ip_dscp_traffic_type"></a>IP \_ DSCP \_ 流量 \_ 類型

下表說明 IP \_ DSCP \_ 流量 \_ 類型通訊端選項。

<dl> <dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**IP \_ DSCP \_ 流量 \_ 類型**</dt> <dd> <dl> <dt> 

| 選項              | Get | 集合 | Optval 類型 | 描述                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DSCP \_ 流量 \_ 類型 | 是 | 是 | DWORD       | 藉由將此值設定為 **DSCP \_ 流量 \_ 類型** 中所定義的值，應用程式將能夠根據所要求的服務類型，要求其網路封包被處理。 同樣地，對 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 的呼叫可以用來取得指定之通訊端上所要求的流量類型目前的設定。 |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|--------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows 10<br/>                                                          |
| 伺服器支援結束<br/> | Windows Server 2016<br/>                                                 |
| 標頭<br/>                | <dl> <dt>N/A</dt> </dl> |



 

 




