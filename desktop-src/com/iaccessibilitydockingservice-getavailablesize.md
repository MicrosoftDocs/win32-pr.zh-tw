---
title: IAccessibilityDockingService GetAvailableSize 方法
description: 取得可在監視器上停駐協助工具視窗的可用維度。
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- GetAvailableSize 方法 COM
- GetAvailableSize 方法 COM，IAccessibilityDockingService 介面
- IAccessibilityDockingService 介面 COM，GetAvailableSize 方法
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022416"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a>IAccessibilityDockingService：： GetAvailableSize 方法

取得可在監視器上停駐協助工具視窗的可用維度。

## <a name="syntax"></a>語法


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMonitor* \[在\]
</dt> <dd>

指定將抓取可用停駐大小的監視器。

</dd> <dt>

*puMaxHeight* \[擴展\]
</dt> <dd>

成功時，請將設定為指定 *hMonitor* 上可停駐的最大高度（以圖元為單位）。

失敗時，請設定為零。

</dd> <dt>

*puFixedWidth* \[擴展\]
</dt> <dd>

成功時，請將設定為固定寬度（可在指定的 *hMonitor* 上銜接）（以圖元為單位）。 停駐至此 *hMonitor* 的任何視窗將會調整為此寬度。

失敗時，請設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值



| 傳回碼                                                                                                                          | Description                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                                 | 成功。<br/>                                                              |
| <dl> <dt>**\_WIN32 中的 HRESULT \_ (錯誤 \_ 不正確 \_ 監視器 \_ 控制碼)**</dt> </dl> | 監視器控制碼所指定的監視器不支援停駐。<br/> |



 

如果 *puMaxHeight* 或 *puFixedWidth* 為 null，則會發生存取違規。

## <a name="remarks"></a>備註

協助工具視窗只能停駐在至少具有768垂直螢幕圖元的監視器上。 此 API 不會允許這類視窗銜接高度，而導致 Windows Store 應用程式的垂直螢幕圖元小於768。

## <a name="examples"></a>範例


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAccessibilityDockingService**](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





