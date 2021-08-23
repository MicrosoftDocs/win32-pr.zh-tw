---
description: 安裝 ActiveX 物件。
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: IeAxiSystemInstaller 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: fb462c4b4f8fc28d9d00de230dea1bbd3670c4fb6eaa962d59875b4fd9054c8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671008"
---
# <a name="ieaxisysteminstaller-interface"></a>IeAxiSystemInstaller 介面

**IeAxiSystemInstaller** 介面會安裝 ActiveX 物件。

未在公用標頭中宣告此介面。 應用程式必須自行定義。 下列介面定義語言 (IDL) 片段描述這個介面，包括其 IID。

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a>成員

**IeAxiSystemInstaller** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IeAxiSystemInstaller** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IeAxiSystemInstaller** 介面具有這些方法。



| 方法                                                                              | 描述                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [**InitializeSystemInstaller**](ieaxisysteminstaller-initializesysteminstaller.md) | 安裝指定的 ActiveX 物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windowsvista Business、Windows vista Enterprise、Windows vista 旗艦版傳統型 \[ 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller 定義為 a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



 

