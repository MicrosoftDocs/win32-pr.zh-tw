---
description: ISCardAuth 介面定義是以標準的形式提供，可在開發智慧卡服務提供者時遵循。ISCardAuth 介面可以用來公開智慧卡所支援的驗證服務。
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: ISCardAuth 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468948"
---
# <a name="iscardauth-interface"></a>ISCardAuth 介面

\[**ISCardAuth** 介面可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ISCardAuth** 介面定義是以標準的形式提供，可在開發 [*智慧卡*](../secgloss/s-gly.md)[*服務提供者*](../secgloss/c-gly.md)時遵循。

**ISCardAuth** 介面可以用來公開智慧卡所支援的驗證服務。 這些服務包括應用程式驗證、智慧卡驗證和使用者驗證。

下列範例顯示 **ISCardAuth** 介面的一般用法。

**使用 ISCardAuth**

1.  透過對應的 [**ISCardManage**](iscardmanage.md)介面方法) 來建立 **ISCardAuth** 介面 (。
2.   ([**應用程式 \_ 驗證**](iscardauth-app-auth.md)、 [**GetChallenge**](iscardauth-getchallenge.md)、 [**ICC \_ 驗證**](iscardauth-icc-auth.md)或 [**使用者 \_ 驗證**](iscardauth-user-auth.md)) ，呼叫適當的 **ISCardAuth** 方法。
3.  釋放 **ISCardAuth** 介面。

## <a name="members"></a>成員

**ISCardAuth** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ISCardAuth** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISCardAuth** 介面具有這些方法。



| 方法                                          | 描述                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**應用程式 \_ 驗證**](iscardauth-app-auth.md)        | 允許應用程式使用挑戰/簽章通訊協定本身進行驗證。<br/> |
| [**GetChallenge**](iscardauth-getchallenge.md) | 從智慧卡傳回挑戰。<br/>                                            |
| [**ICC \_ 驗證**](iscardauth-icc-auth.md)        | 允許應用程式驗證智慧卡。<br/>                               |
| [**使用者 \_ 驗證**](iscardauth-user-auth.md)      | 允許存取使用者驗證服務。<br/>                                      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows XP<br/>                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                       |



 

 
