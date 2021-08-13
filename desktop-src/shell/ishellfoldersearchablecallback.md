---
description: 公開回呼常式來監視搜尋處理常式。
title: IShellFolderSearchableCallback 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3412a01b-d5ea-44e1-819c-f10f81fac391
ms.openlocfilehash: 620acb5d5a3486b721cac3818c57b8392174436f68a304a8788ef62bccae28b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443288"
---
# <a name="ishellfoldersearchablecallback-interface"></a>IShellFolderSearchableCallback 介面

公開回呼常式來監視搜尋處理常式。

## <a name="members"></a>成員

**IShellFolderSearchableCallback** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IShellFolderSearchableCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IShellFolderSearchableCallback** 介面具有這些方法。



| 方法                                                      | 描述                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [**RunBegin**](ishellfoldersearchablecallback-runbegin.md) | 表示搜尋已啟動。<br/>  |
| [**RunEnd**](ishellfoldersearchablecallback-runend.md)     | 表示搜尋已完成。<br/> |



 

## <a name="remarks"></a>備註

這個介面未定義在任何公用標頭檔中。 如果您選擇執行這個介面，您可以使用下列 C/c + + 程式碼來宣告其方法。


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchableCallback Methods ***

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
