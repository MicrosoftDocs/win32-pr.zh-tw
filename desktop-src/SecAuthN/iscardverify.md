---
description: 提供用來設定 CHV (卡持有者驗證) 碼以及驗證使用者的服務。
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: ISCardVerify 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: e2f676360636395e0df811abed225c1a53be69a7da07f38a8acb08fc8d45e2ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141011"
---
# <a name="iscardverify-interface"></a>ISCardVerify 介面

\[**ISCardVerify** 介面可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

下列介面定義是以標準的形式提供，可在開發 [*智慧卡*](../secgloss/s-gly.md)[*服務提供者*](../secgloss/c-gly.md)時遵循。 **ISCardVerify** 介面提供了用來設定 CHV (卡持有者驗證) 碼以及驗證使用者的服務。

**ISCardVerify** 類別是針對執行應用程式專屬 CHV 原則的應用程式所定義，且具有智慧卡內部執行的詳細知識。

以下是 **ISCardVerify** 介面的一般用法。

下列程式會使用 **ISCardVerify** 來變更 CHV 程式碼。

**變更智慧卡的 CHV 碼**

1.  透過對應的 [**ISCardManage**](iscardmanage.md)介面方法) 來建立 **ISCardVerify** 介面 (。
2.  呼叫 [**ChangeCode**](iscardverify-changecode.md) 方法，並提供新的程式碼，並指定其為本機或全域，以及啟用或停用。
3.  釋放 **ISCardVerify** 介面。

## <a name="members"></a>成員

**ISCardVerify** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ISCardVerify** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISCardVerify** 介面具有這些方法。



| 方法                                                        | 描述                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeCode**](iscardverify-changecode.md)                 | 變更目前的 CHV 碼。<br/>                                                                                                    |
| [**ResetSecurityState**](iscardverify-resetsecuritystate.md) | 重設智慧卡的 [*安全性內容*](../secgloss/s-gly.md) 。<br/> |
| [**疏通**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))                       | 重新啟用 [*安全性內容*](../secgloss/s-gly.md)。<br/>               |
| [**驗證**](iscardverify-verify.md)                         | 驗證使用者。<br/>                                                                                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows XP<br/>                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                       |



 

 
