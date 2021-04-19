---
title: IMsRdpClientTransportSettings GatewayUsageMethod 屬性
description: 指定使用遠端桌面閘道 (RD 閘道) server 的時機。
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- GatewayUsageMethod 屬性遠端桌面服務
- GatewayUsageMethod 屬性遠端桌面服務，IMsRdpClientTransportSettings 介面
- IMsRdpClientTransportSettings 介面遠端桌面服務，GatewayUsageMethod 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966097"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a>IMsRdpClientTransportSettings：： GatewayUsageMethod 屬性

指定使用遠端桌面閘道 (RD 閘道) server 的時機。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a>屬性值

指定 RD 閘道伺服器使用方法的 **ULONG** 變數。 此參數可以是下列其中一個值。

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_PROXY \_ 模式 \_ 無 \_ 直接** (0 (0x0) ) 


</dt> <dd>

請勿使用 RD 閘道的伺服器。 在遠端桌面連線 (RDC) 用戶端 UI 中，已清除 [ **本機位址略過 RD 閘道伺服器** ] 核取方塊。

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_PROXY \_ 模式 \_ 直接** (1 (0x1) ) 


</dt> <dd>

一律使用 RD 閘道伺服器。 在 RDC 用戶端 UI 中，[ **本機位址略過 RD 閘道伺服器** ] 核取方塊已清除。

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_PROXY \_ 模式 \_** 偵測 (2 (0x2) ) 


</dt> <dd>

如果無法直接連接到 RD 工作階段主機伺服器，請使用 RD 閘道伺服器。 在 RDC 用戶端 UI 中，已選取 [ **略過本機位址的 RD 閘道伺服器** ] 核取方塊。

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_PROXY \_ 模式 \_ 預設** (3 (0x3) ) 


</dt> <dd>

使用預設 RD 閘道伺服器設定。

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_PROXY \_ 模式 \_ NONE \_** 偵測 (4 (0x4) ) 


</dt> <dd>

請勿使用 RD 閘道的伺服器。 在 RDC 用戶端 UI 中，已選取 [ **略過本機位址的 RD 閘道伺服器** ] 核取方塊。

</dd> </dl>

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings 定義為720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





