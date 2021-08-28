---
title: 'D2D1CreateFactory Factory (D2D1_FACTORY_TYPE，Factory ) 函式 (D2d1 .h) '
description: '建立可用於建立 Direct2D 資源的 factory 物件。 |D2D1CreateFactory Factory (D2D1_FACTORY_TYPE，Factory ) 函式 (D2d1 .h) '
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE，Factory ) 函數 Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f36a5fd244f0dc814de2414b5642fc4f57ca744a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883260"
---
# <a name="d2d1createfactoryltfactorygtd2d1_factory_typefactory-function"></a>D2D1CreateFactory &lt; factory &gt; (D2D1 \_ Factory \_ 類型，factory \* \*) 函數

建立可用於建立 Direct2D 資源的 factory 物件。

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>範本參數



| 參數 | 說明                                                 |
|-----------|-------------------------------------------------------------|
| *廠* | 要建立之 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 的類型。 |



 

## <a name="parameters"></a>參數



| 參數     | 說明                                                                     |
|---------------|---------------------------------------------------------------------------------|
| *factoryType* | Factory 的執行緒模型和它所建立的資源。                |
| *工廠*     | 當此方法傳回時，會包含指向新 factory 之指標的位址。 |



 

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="examples"></a>範例

下列範例會建立一個 factory。


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、Windows vista （含 SP2），以及適用于 Windows Vista \[ desktop apps \| UWP 應用程式的平臺更新\]<br/>                          |
| 最低支援的伺服器<br/> | Windowsserver 2008 R2、Windows server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>D2d1。h</dt> </dl>                                                        |
| 程式庫<br/>                  | <dl> <dt>D2d1 .lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

