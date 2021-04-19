---
description: 若要讓認證安全性支援提供者通訊協定 (CredSSP) 委派認證，您必須指定可委派給哪些伺服器。
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: CredSSP 群組原則設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987634"
---
# <a name="credssp-group-policy-settings"></a><span data-ttu-id="4466f-103">CredSSP 群組原則設定</span><span class="sxs-lookup"><span data-stu-id="4466f-103">CredSSP Group Policy Settings</span></span>

<span data-ttu-id="4466f-104">若要讓 [認證安全性支援提供者通訊協定 (CredSSP) ](credential-security-support-provider.md) 委派認證，您必須指定可委派給哪些伺服器。</span><span class="sxs-lookup"><span data-stu-id="4466f-104">For [Credential Security Support Provider protocol (CredSSP)](credential-security-support-provider.md) to delegate credentials, you must specify which servers can be delegated to.</span></span> <span data-ttu-id="4466f-105">若要指定這些伺服器，請修改群組原則編輯器中的設定 (GPE) Microsoft Management Console (MMC) 嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="4466f-105">To specify those servers, modify settings in the Group Policy Editor (GPE) Microsoft Management Console (MMC) snap-in.</span></span> <span data-ttu-id="4466f-106">控制委派的 GPE 設定位於 [電腦設定] 底下， **\| 系統管理範本 \| 系統 \| 認證委派**。</span><span class="sxs-lookup"><span data-stu-id="4466f-106">The GPE settings that control delegation are under **Computer Configuration \| Administrative Templates \| System \| Credentials Delegation**.</span></span>

> [!Caution]  
> <span data-ttu-id="4466f-107">這不是限制委派。</span><span class="sxs-lookup"><span data-stu-id="4466f-107">This is not constrained delegation.</span></span> <span data-ttu-id="4466f-108">CredSSP 會將使用者的完整認證傳遞給沒有任何條件約束的伺服器。</span><span class="sxs-lookup"><span data-stu-id="4466f-108">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="4466f-109">群組原則設定會控制下列認證類型的委派。</span><span class="sxs-lookup"><span data-stu-id="4466f-109">Group policy settings control delegation of the following types of credentials.</span></span>



| <span data-ttu-id="4466f-110">認證類型</span><span class="sxs-lookup"><span data-stu-id="4466f-110">Credentials Type</span></span>                                                                                                                                 | <span data-ttu-id="4466f-111">Description</span><span class="sxs-lookup"><span data-stu-id="4466f-111">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4466f-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>預設認證</span><span class="sxs-lookup"><span data-stu-id="4466f-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Default credentials</span></span><br/> | <span data-ttu-id="4466f-113">使用者第一次登入 Windows 時所取得的認證。</span><span class="sxs-lookup"><span data-stu-id="4466f-113">The credentials obtained when the user first logs on to Windows.</span></span><br/>                   |
| <span data-ttu-id="4466f-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>新認證</span><span class="sxs-lookup"><span data-stu-id="4466f-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Fresh credentials</span></span><br/>         | <span data-ttu-id="4466f-115">當使用者執行應用程式時，系統會提示使用者輸入認證。</span><span class="sxs-lookup"><span data-stu-id="4466f-115">The credentials that the user is prompted for when executing an application.</span></span><br/>       |
| <span data-ttu-id="4466f-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>儲存的認證</span><span class="sxs-lookup"><span data-stu-id="4466f-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Saved credentials</span></span><br/>         | <span data-ttu-id="4466f-117">使用 [認證管理員](credential-manager.md)儲存的認證。</span><span class="sxs-lookup"><span data-stu-id="4466f-117">The credentials that are saved using [Credential Manager](credential-manager.md).</span></span><br/> |



 

<span data-ttu-id="4466f-118">若要在與特定群組原則設定相關聯的類別中包含伺服器，請將該伺服器的 [*服務主體名稱*](/windows/desktop/SecGloss/s-gly) (SPN) 新增至該群組原則設定的伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="4466f-118">To include a server in the category associated with a particular group policy setting, add the [*Service Principal Name*](/windows/desktop/SecGloss/s-gly) (SPN) of that server to the list of servers for that group policy setting.</span></span> <span data-ttu-id="4466f-119">SPN 可以包含單一萬用字元。</span><span class="sxs-lookup"><span data-stu-id="4466f-119">The SPN can contain a single wildcard character.</span></span>

 

