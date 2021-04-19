---
description: 當目前的使用者沒有安裝物件的許可權時，初始化系統服務物件以安裝 ActiveX 物件。
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: IeAxiService 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001404"
---
# <a name="ieaxiservice-interface"></a>IeAxiService 介面

當目前的使用者沒有安裝物件的許可權時， **IAxiService** 介面會初始化系統服務物件以安裝 ActiveX 物件。

[**CIeAxiInstallerService**](cieaxiinstallerservice.md)類別會執行這個介面。

未在公用標頭中宣告此介面。 應用程式必須自行定義。 下列介面定義語言 (IDL) 片段描述這個介面，包括其 IID。

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a>成員

**IeAxiService** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IeAxiService** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IeAxiService** 介面具有這些方法。



| 方法                                        | 描述                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [**清除**](ieaxiservice-cleanup.md)       | 釋放 **IeAxiService** 介面使用的資源。<br/> |
| [**初始化**](ieaxiservice-initialize.md) | 檢查和下載 ActiveX 物件。<br/>                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService 定義為 E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



 

