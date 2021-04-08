---
description: 由 IeAxiSystemInstaller 介面呼叫，以確認可以安裝 ActiveX 物件。
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: IeAxiServiceCallback 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852908"
---
# <a name="ieaxiservicecallback-interface"></a>IeAxiServiceCallback 介面

**IeAxiServiceCallback** 介面會由 [**IeAxiSystemInstaller**](ieaxisysteminstaller.md)介面呼叫，以確認可以安裝 ActiveX 物件。

[**CIeAxiInstallerService**](cieaxiinstallerservice.md)類別會執行這個介面。

未在公用標頭中宣告此介面。 應用程式必須自行定義。 下列介面定義語言 (IDL) 片段描述這個介面，包括其 IID。

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a>成員

**IeAxiServiceCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IeAxiServiceCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IeAxiServiceCallback** 介面具有這些方法。



| 方法                                                | 描述                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**VerifyFile**](ieaxiservicecallback-verifyfile.md) | 針對指定的 ActiveX 物件執行安全性檢查，並傳回下載對應 .cab 檔案的位置。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback 定義為1823E7BA-EC36-447a-9B2E-B4912E15AFE7<br/>                   |



 

