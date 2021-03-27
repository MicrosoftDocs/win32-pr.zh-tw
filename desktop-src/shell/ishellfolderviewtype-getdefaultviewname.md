---
description: 取得預設視圖的名稱。 呼叫 GetDisplayNameOf 以取得其他視圖的名稱。
title: IShellFolderViewType：： GetDefaultViewName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 239fcd80bcfc0b29287f8e16aeef3efb8ae032c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972341"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a>IShellFolderViewType：： GetDefaultViewName 方法

取得預設視圖的名稱。 呼叫 [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 以取得其他視圖的名稱。

## <a name="syntax"></a>語法


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*uFlags* \[在\]
</dt> <dd>

類型： **DWORD**

選擇性旗標;應設定為0。

</dd> <dt>

*ppwszName* \[擴展\]
</dt> <dd>

類型： **LPWSTR \** _

接收預設視圖名稱之字串指標的位址。 字串的記憶體是使用 [_ *SHStrDup* *](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)來配置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




