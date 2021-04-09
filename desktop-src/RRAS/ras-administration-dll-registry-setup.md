---
title: 關於 RAS 管理 DLL 登錄設定
description: 協力廠商 RAS 管理 DLL 的安裝程式必須在登錄中的下列機碼底下提供資訊，向 RAS 註冊 DLL。
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RAS 管理 RRAS，DLL 登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf487f792a4add9ebf61e8f866b9f0577fb468d
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "103841712"
---
# <a name="about-ras-administration-dll-registry-setup"></a><span data-ttu-id="2ec41-104">關於 RAS 管理 DLL 登錄設定</span><span class="sxs-lookup"><span data-stu-id="2ec41-104">About RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="2ec41-105">協力廠商 RAS 管理 DLL 的安裝程式必須在登錄中的下列機碼底下提供資訊，向 RAS 註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="2ec41-105">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="2ec41-106">若要註冊 DLL，請在此機碼下設定下列值。</span><span class="sxs-lookup"><span data-stu-id="2ec41-106">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="2ec41-107">值名稱</span><span class="sxs-lookup"><span data-stu-id="2ec41-107">Value name</span></span>    | <span data-ttu-id="2ec41-108">值資料</span><span class="sxs-lookup"><span data-stu-id="2ec41-108">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="2ec41-109">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="2ec41-109">*DisplayName*</span></span> | <span data-ttu-id="2ec41-110">**REG \_ SZ** 字串，其中包含 DLL 的使用者易記顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2ec41-110">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="2ec41-111">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="2ec41-111">*DLLPath*</span></span>     | <span data-ttu-id="2ec41-112">**REG \_ SZ** 字串，其中包含 DLL 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2ec41-112">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="2ec41-113">由於 RAS 支援多個 RAS 管理 Dll，因此登錄值 **DLLPath** 可以包含以分號分隔的路徑清單。</span><span class="sxs-lookup"><span data-stu-id="2ec41-113">Because RAS supports multiple RAS Administration DLLs, the registry value **DLLPath** can contain a semi-colon delimited list of paths.</span></span> <span data-ttu-id="2ec41-114">例如，名為 ProElectron，Inc. 之虛構公司的 RAS 管理 DLL 的登錄專案可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="2ec41-114">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc., might be the following:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="2ec41-115">*DisplayName*： **REG \_ SZ** ： ProElectron RAS 管理 DLL</span><span class="sxs-lookup"><span data-stu-id="2ec41-115">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="2ec41-116">*DLLPath*： **REG \_ SZ** ： C： \\ nt \\ system32 \\ntwkadm.dll;C： \\ nt \\ system32 \\ntwkadm2.dll</span><span class="sxs-lookup"><span data-stu-id="2ec41-116">*DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll; C:\\nt\\system32\\ntwkadm2.dll</span></span>

<span data-ttu-id="2ec41-117">RAS 會依此登錄值列出 Dll 的順序來呼叫它們。</span><span class="sxs-lookup"><span data-stu-id="2ec41-117">RAS calls the DLLs in the order in which they are listed in this registry value.</span></span> <span data-ttu-id="2ec41-118">登錄值 *DisplayName* 仍只包含單一顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2ec41-118">The registry value *DisplayName* still contains only a single display name.</span></span>

<span data-ttu-id="2ec41-119">RAS 系統管理 DLL 的安裝程式也必須提供移除和卸載功能。</span><span class="sxs-lookup"><span data-stu-id="2ec41-119">The setup program for a RAS administration DLL must also provide remove and uninstall functionality.</span></span> <span data-ttu-id="2ec41-120">如果使用者移除 DLL，安裝程式必須刪除 DLL 的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="2ec41-120">If a user removes the DLL, the setup program must delete the registry entries for the DLL.</span></span>

<span data-ttu-id="2ec41-121">**Windows 2000/NT：** RAS 只支援一個 RAS 管理 DLL，因此登錄值 **DLLPath** 不能包含以分號分隔的路徑清單。</span><span class="sxs-lookup"><span data-stu-id="2ec41-121">**Windows 2000/NT:** RAS supports only one RAS Administration DLL, so the registry value **DLLPath** cannot contain a semi-colon delimited list of paths.</span></span>

 

 




