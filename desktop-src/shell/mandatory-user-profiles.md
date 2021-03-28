---
description: 強制使用者設定檔是一種特殊的預先設定漫遊使用者設定檔，可讓系統管理員用來指定使用者的設定。
title: 強制使用者設定檔
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 744d35e92a279c5d8a8e8b239fa64bb1960e011a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510767"
---
# <a name="mandatory-user-profiles"></a><span data-ttu-id="beedc-103">強制使用者設定檔</span><span class="sxs-lookup"><span data-stu-id="beedc-103">Mandatory User Profiles</span></span>

<span data-ttu-id="beedc-104">強制使用者設定檔是一種特殊的預先設定 [漫遊使用者設定檔](roaming-user-profiles.md) ，可讓系統管理員用來指定使用者的設定。</span><span class="sxs-lookup"><span data-stu-id="beedc-104">A mandatory user profile is a special type of pre-configured [roaming user profile](roaming-user-profiles.md) that administrators can use to specify settings for users.</span></span> <span data-ttu-id="beedc-105">使用強制使用者設定檔時，使用者可以修改其桌面，但當使用者登出時，不會儲存變更。</span><span class="sxs-lookup"><span data-stu-id="beedc-105">With mandatory user profiles, a user can modify his or her desktop, but the changes are not saved when the user logs off.</span></span> <span data-ttu-id="beedc-106">使用者下一次登入時，系統會下載系統管理員所建立的強制使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="beedc-106">The next time the user logs on, the mandatory user profile created by the administrator is downloaded.</span></span> <span data-ttu-id="beedc-107">強制設定檔有兩種類型： *標準強制* 設定檔和 *超級強制* 設定檔。</span><span class="sxs-lookup"><span data-stu-id="beedc-107">There are two types of mandatory profiles: *normal mandatory* profiles and *super-mandatory* profiles.</span></span>

<span data-ttu-id="beedc-108">當系統管理員將伺服器上的 Ntuser.man 登錄區)  (登錄 hive 時，使用者設定檔會變成強制設定檔，以 Ntuser.man。</span><span class="sxs-lookup"><span data-stu-id="beedc-108">User profiles become mandatory profiles when the administrator renames the NTuser.dat file (the registry hive) on the server to NTuser.man.</span></span> <span data-ttu-id="beedc-109">Man 延伸會使使用者設定檔成為唯讀設定檔。</span><span class="sxs-lookup"><span data-stu-id="beedc-109">The .man extension causes the user profile to be a read-only profile.</span></span>

<span data-ttu-id="beedc-110">當設定檔路徑的資料夾名稱結束時，使用者設定檔會變成 *超級強制性*。例如， \\ \\ server \\ share \\ mandatoryprofile。 \\</span><span class="sxs-lookup"><span data-stu-id="beedc-110">User profiles become *super-mandatory* when the folder name of the profile path ends in .man; for example, \\\\server\\share\\mandatoryprofile.man\\.</span></span>

<span data-ttu-id="beedc-111">超級強制使用者設定檔類似于一般的強制設定檔，例外狀況是當儲存強制設定檔的伺服器無法使用時，具有超級強制設定檔的使用者無法登入。</span><span class="sxs-lookup"><span data-stu-id="beedc-111">Super-mandatory user profiles are similar to normal mandatory profiles, with the exception that users who have super-mandatory profiles cannot log on when the server that stores the mandatory profile is unavailable.</span></span> <span data-ttu-id="beedc-112">具有一般強制設定檔的使用者可以使用強制設定檔的本機快取複本來登入。</span><span class="sxs-lookup"><span data-stu-id="beedc-112">Users with normal mandatory profiles can log on with the locally cached copy of the mandatory profile.</span></span>

<span data-ttu-id="beedc-113">只有系統管理員可以對強制使用者設定檔進行變更。</span><span class="sxs-lookup"><span data-stu-id="beedc-113">Only system administrators can make changes to mandatory user profiles.</span></span>

 

 



