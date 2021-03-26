---
UID: ''
title: SHIsChildOrSelf 函式
description: 比較視窗是否等於第二個視窗的子系、的子系或子代。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "104990875"
---
# <a name="shischildorself-function"></a>SHIsChildOrSelf 函式

## <a name="description"></a>Description

\[這項功能可透過 Windows XP 和 Windows Server 2003 取得。
它可能會在後續版本的 Windows 中改變或無法使用。\]

比較視窗是否等於第二個視窗的子系、的子系或子代。

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a>參數

### <a name="hwndparent-in"></a>hwndParent [in]

類型： **HWND**

第一個視窗的控制碼。

### <a name="hwnd-in"></a>hwnd [in]

類型： **HWND**

要針對 *hwndParent* 進行測試的視窗控制碼。

## <a name="returns"></a>傳回

類型： **HRESULT**

如果 *hwnd* 指定的視窗等於、的子系或 *hwndParent* 所指定視窗的子系，則會傳回 **S_OK** 。
如果 hwnd 指定的視窗不等於、非的子系，而不是 *hwndParent* 所指定視窗的子系，則會傳回 **S_FALSE** 。
如果任一視窗控制碼無效，則傳回值為未定義。

## <a name="remarks"></a>備註

## <a name="see-also"></a>另請參閱

[IsChild](/windows/desktop/api/winuser/nf-winuser-ischild)
