---
description: Microsoft SMB 通訊協定中所使用的安全性模型與其他 SMB 變數所使用的模型相同，且包含兩個層級的安全性&\# 郵件; 使用者和共用。
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Microsoft SMB 通訊協定驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847967"
---
# <a name="microsoft-smb-protocol-authentication"></a><span data-ttu-id="c5c80-103">Microsoft SMB 通訊協定驗證</span><span class="sxs-lookup"><span data-stu-id="c5c80-103">Microsoft SMB Protocol Authentication</span></span>

<span data-ttu-id="c5c80-104">Microsoft SMB 通訊協定中使用的安全性模型與其他 SMB 變數所使用的模型相同，且包含兩種安全性層級：使用者和共用。</span><span class="sxs-lookup"><span data-stu-id="c5c80-104">The security model used in Microsoft SMB Protocol is identical to the one used by other variants of SMB, and consists of two levels of security—user and share.</span></span> <span data-ttu-id="c5c80-105">共用是可由 Microsoft SMB 通訊協定用戶端存取的檔案、目錄或印表機。</span><span class="sxs-lookup"><span data-stu-id="c5c80-105">A share is a file, directory, or printer that can be accessed by Microsoft SMB Protocol clients.</span></span>

<span data-ttu-id="c5c80-106">使用者層級驗證表示嘗試存取伺服器上共用的用戶端必須提供使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="c5c80-106">User-level authentication indicates that the client attempting to access a share on a server must provide a user name and password.</span></span> <span data-ttu-id="c5c80-107">經過驗證之後，使用者就可以存取未受共用層級安全性保護的伺服器上的所有共用。</span><span class="sxs-lookup"><span data-stu-id="c5c80-107">When authenticated, the user can then access all shares on a server not also protected by share-level security.</span></span> <span data-ttu-id="c5c80-108">此安全性層級可讓系統管理員明確地判斷哪些使用者和群組可以存取共用。</span><span class="sxs-lookup"><span data-stu-id="c5c80-108">This security level allows system administrators to specifically determine which users and groups can access a share.</span></span>

<span data-ttu-id="c5c80-109">共用層級驗證表示共用的存取權是由僅指派給該共用的密碼所控制。</span><span class="sxs-lookup"><span data-stu-id="c5c80-109">Share-level authentication indicates that access to a share is controlled by a password assigned to that share only.</span></span> <span data-ttu-id="c5c80-110">不同于使用者層級安全性，此安全性等級不需要使用者名稱進行驗證，也不會建立使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="c5c80-110">Unlike user-level security, this security level does not require a user name for authentication and no user identity is established.</span></span>

<span data-ttu-id="c5c80-111">在這兩個安全性層級下，密碼會在傳送到伺服器之前進行加密。</span><span class="sxs-lookup"><span data-stu-id="c5c80-111">Under both of these security levels, the password is encrypted before it is sent to the server.</span></span> <span data-ttu-id="c5c80-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) 和舊版 LAN MANAGER (LM) 加密受到 Microsoft SMB 通訊協定的支援。</span><span class="sxs-lookup"><span data-stu-id="c5c80-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) and the older LAN Manager (LM) encryption are supported by Microsoft SMB Protocol.</span></span> <span data-ttu-id="c5c80-113">這兩種加密方法都使用挑戰回應驗證，在此驗證中，伺服器會將隨機字串傳送給用戶端，而用戶端則會傳回可證明用戶端有足夠認證可供存取的計算回應字串。</span><span class="sxs-lookup"><span data-stu-id="c5c80-113">Both encryption methods use challenge-response authentication, where the server sends the client a random string and the client returns a computed response string that proves the client has sufficient credentials for access.</span></span>

 

 
