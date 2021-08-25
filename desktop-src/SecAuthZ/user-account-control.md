---
description: 可讓使用者以非系統管理員（稱為標準使用者）和系統管理員身分執行一般工作，而不需要切換使用者、登出或使用 [執行身分]。
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: " (授權) 的使用者帳戶控制"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da0092ed5d8de1c141ba4ee2ea31a498bd6954ba8401aafeb08e6a69b8d130f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906828"
---
# <a name="user-account-control-authorization"></a> (授權) 的使用者帳戶控制

 (UAC) 的使用者帳戶控制可讓使用者以非系統管理員的身分（稱為標準使用者）或系統管理員身分執行一般工作，而不需要切換使用者、登出或使用 [ **執行** 身分]。 「永不通知」設定的 UAC 行為不再停用 UAC。 [永不通知] 設定會提供您一個分割權杖，而且一律會自動提升所需的許可權。 此奧妙可能會導致您的應用程式發生相容性問題。 您仍然可以使用群組原則或手動設定登錄機碼來停用 UAC。

**Windows server 2008 R2、Windows 7、Windows Server 2008 和 Windows Vista：**[永不通知] 設定會停用 UAC。

例如，如果您執行下列步驟來變更 [永遠不要通知] 設定，當您嘗試在需要提高許可權的資料夾中建立檔案時，就會得到不同的結果。 Windows 8 行為是拒絕存取。 Windows 7 的行為可讓您建立 File.txt 檔案。

1.  按一下或點擊 [ **開始**]。 在搜尋方塊中，輸入「變更使用者帳戶控制設定」。
2.  按一下或按一下 [ **變更使用者帳戶控制設定** ] 以開啟它。
3.  將滑杆移至 [ **永不通知**]。
4.  按一下或點擊 **[確定]**。
5.  重新啟動您的電腦。
6.  按一下或按一下 [ **開始** ]，然後 **執行**。 在 [ **開啟** ] 方塊中，輸入 "Cmd.exe"。 請注意，視窗的標題不包含 "Administrator" 字串。
7.  輸入「echo >% windir% \\ system32 \\File.txt」。

UAC 已新增至 Windows Server 2008 和 Windows Vista。 標準使用者帳戶與 Windows XP 中的使用者帳戶同義。 屬於本機 Administrators 群組成員的使用者帳戶將以標準使用者的身分執行大部分的應用程式。

如需 UAC 的詳細資訊，請參閱下列主題。



| 主題                                                                                                                                        | 描述                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [UI 開發中的使用者帳戶控制指導方針](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)<br/> | UAC 的一般資訊。<br/>                                                                                                     |
| [開發需要系統管理員許可權的應用程式](developing-applications-that-require-administrator-privilege.md)<br/>  | 適用于開發應用程式的模型，這些應用程式會執行需要系統管理許可權，但以標準使用者的身份執行的作業。<br/> |
| [授權參考](authorization-reference.md)<br/>                                                                            | 授權函數、介面、結構和其他程式設計專案的詳細資訊。<br/>                        |



 

 

 




