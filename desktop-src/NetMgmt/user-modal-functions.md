---
title: 使用者模式函數
description: 網路管理使用者強制回應功能會取得並設定與安全性系統行為相關的全系統參數。
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933546"
---
# <a name="user-modal-functions"></a><span data-ttu-id="dd869-103">使用者模式函數</span><span class="sxs-lookup"><span data-stu-id="dd869-103">User Modal Functions</span></span>

<span data-ttu-id="dd869-104">網路管理使用者強制回應功能會取得並設定與安全性系統行為相關的全系統參數。</span><span class="sxs-lookup"><span data-stu-id="dd869-104">The network management user modal functions get and set system-wide parameters related to security system behavior.</span></span>

<span data-ttu-id="dd869-105">使用者模式函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="dd869-105">The user modal functions are listed following.</span></span>



| <span data-ttu-id="dd869-106">函式</span><span class="sxs-lookup"><span data-stu-id="dd869-106">Function</span></span>                                     | <span data-ttu-id="dd869-107">描述</span><span class="sxs-lookup"><span data-stu-id="dd869-107">Description</span></span>                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd869-108">**NetUserModalsGet**</span><span class="sxs-lookup"><span data-stu-id="dd869-108">**NetUserModalsGet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | <span data-ttu-id="dd869-109">傳回安全性資料庫中所有使用者和全域群組的全域資訊，也就是安全性帳戶管理員 (SAM) 資料庫，或在網域控制站的情況下 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="dd869-109">Returns global information for all users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.</span></span> |
| [<span data-ttu-id="dd869-110">**NetUserModalsSet**</span><span class="sxs-lookup"><span data-stu-id="dd869-110">**NetUserModalsSet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | <span data-ttu-id="dd869-111">針對安全性資料庫中的所有使用者和全域群組設定全域資訊。</span><span class="sxs-lookup"><span data-stu-id="dd869-111">Sets global information for all users and global groups in the security database.</span></span>                                                                                                                       |



 

<span data-ttu-id="dd869-112">**NetUserModalsGet** 和 **NetUserModalsSet** 函式會檢查和修改強制回應設定，這些設定是影響安全性資料庫中每個帳戶的全域參數 (例如，允許的最小密碼長度) 。</span><span class="sxs-lookup"><span data-stu-id="dd869-112">The **NetUserModalsGet** and **NetUserModalsSet** functions examine and modify the modal settings, which are global parameters that affect every account in the security database (for example, the minimum allowable password length).</span></span> <span data-ttu-id="dd869-113">您可以藉由呼叫 **NetUserModalsSet** 來改變所有強制回應設定。</span><span class="sxs-lookup"><span data-stu-id="dd869-113">All modal settings can be altered by calling **NetUserModalsSet**.</span></span> <span data-ttu-id="dd869-114">您也可以使用 **net accounts** 命令來改變大部分的 modals。</span><span class="sxs-lookup"><span data-stu-id="dd869-114">Most of the modals can also be altered by using the **net accounts** command.</span></span> <span data-ttu-id="dd869-115">網路管理使用者強制回應功能不需要伺服器擁有使用者層級安全性。</span><span class="sxs-lookup"><span data-stu-id="dd869-115">The network management user modal functions do not require the server to have user-level security.</span></span>

<span data-ttu-id="dd869-116">使用者模式資訊可在下列層級取得：</span><span class="sxs-lookup"><span data-stu-id="dd869-116">User modal information is available at the following levels:</span></span>

-   [<span data-ttu-id="dd869-117">**使用者 \_ MODALS \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="dd869-117">**USER\_MODALS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [<span data-ttu-id="dd869-118">**使用者 \_ MODALS \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="dd869-118">**USER\_MODALS\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [<span data-ttu-id="dd869-119">**使用者 \_ MODALS \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="dd869-119">**USER\_MODALS\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [<span data-ttu-id="dd869-120">**使用者 \_ MODALS \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="dd869-120">**USER\_MODALS\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

<span data-ttu-id="dd869-121">下列資訊層級僅適用于 [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) ，並取代較舊的方法來傳遞 *Parmnum* 來設定特定欄位：</span><span class="sxs-lookup"><span data-stu-id="dd869-121">The following information levels are valid only for [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) and replace the older way of passing in a *Parmnum* to set a specific field:</span></span>

-   [<span data-ttu-id="dd869-122">**使用者 \_ MODALS \_ 資訊 \_ 1001**</span><span class="sxs-lookup"><span data-stu-id="dd869-122">**USER\_MODALS\_INFO\_1001**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [<span data-ttu-id="dd869-123">**使用者 \_ MODALS \_ 資訊 \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="dd869-123">**USER\_MODALS\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [<span data-ttu-id="dd869-124">**使用者 \_ MODALS \_ 資訊 \_ 1003**</span><span class="sxs-lookup"><span data-stu-id="dd869-124">**USER\_MODALS\_INFO\_1003**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [<span data-ttu-id="dd869-125">**使用者 \_ MODALS \_ 資訊 \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="dd869-125">**USER\_MODALS\_INFO\_1004**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [<span data-ttu-id="dd869-126">**使用者 \_ MODALS \_ 資訊 \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="dd869-126">**USER\_MODALS\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [<span data-ttu-id="dd869-127">**使用者 \_ MODALS \_ 資訊 \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="dd869-127">**USER\_MODALS\_INFO\_1006**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [<span data-ttu-id="dd869-128">**使用者 \_ MODALS \_ 資訊 \_ 1007**</span><span class="sxs-lookup"><span data-stu-id="dd869-128">**USER\_MODALS\_INFO\_1007**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

<span data-ttu-id="dd869-129">如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以達到您可以藉由呼叫網路管理使用者模式函式達成的相同功能。</span><span class="sxs-lookup"><span data-stu-id="dd869-129">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user modal functions.</span></span> <span data-ttu-id="dd869-130">如需詳細資訊，請參閱 [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain)。</span><span class="sxs-lookup"><span data-stu-id="dd869-130">For more information, see [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span></span>

 

 