---
title: Role 屬性
description: Role 屬性描述物件的使用者介面元素。 所有物件都支援 Role 屬性。
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f2b285d9242542f83c6b4478df93e888a7a23cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996146"
---
# <a name="role-property"></a><span data-ttu-id="35c77-104">Role 屬性</span><span class="sxs-lookup"><span data-stu-id="35c77-104">Role Property</span></span>

<span data-ttu-id="35c77-105">**Role** 屬性描述物件的使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="35c77-105">The **Role** property describes an object's user interface element.</span></span> <span data-ttu-id="35c77-106">所有物件都支援 **Role** 屬性。</span><span class="sxs-lookup"><span data-stu-id="35c77-106">All objects support the **Role** property.</span></span>

<span data-ttu-id="35c77-107">在許多情況下，物件的角色很明顯。</span><span class="sxs-lookup"><span data-stu-id="35c77-107">In many cases, the object's role is obvious.</span></span> <span data-ttu-id="35c77-108">例如，windows 具有 [**角色 \_ 系統 \_ 視窗**](object-roles.md) 角色，而推送按鈕具有 [**角色 \_ 系統 \_ 按鈕**](object-roles.md) 角色。</span><span class="sxs-lookup"><span data-stu-id="35c77-108">For example, windows have the [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) role and push buttons have the [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md) role.</span></span>

<span data-ttu-id="35c77-109">藉由呼叫 [**IAccessible：： get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)來抓取 **Role** 屬性。</span><span class="sxs-lookup"><span data-stu-id="35c77-109">The **Role** property is retrieved by calling [**IAccessible::get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span></span>

## <a name="identifying-an-objects-role"></a><span data-ttu-id="35c77-110">識別物件的角色</span><span class="sxs-lookup"><span data-stu-id="35c77-110">Identifying an Object's Role</span></span>

<span data-ttu-id="35c77-111">Microsoft Active Accessibility 提供定義于 oleacc 中的 [角色常數](object-roles.md)，用以識別通用物件角色。</span><span class="sxs-lookup"><span data-stu-id="35c77-111">Microsoft Active Accessibility provides [role constants](object-roles.md), defined in oleacc.h, that identify common object roles.</span></span> <span data-ttu-id="35c77-112">建議伺服器開發人員使用這些預先定義的角色值。</span><span class="sxs-lookup"><span data-stu-id="35c77-112">It is recommended that server developers use these predefined role values.</span></span> <span data-ttu-id="35c77-113">如果傳回預先定義的角色常數，用戶端會使用 [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) 函式來取得描述角色的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="35c77-113">If a predefined role constant is returned, clients use the [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) function to retrieve a localized string that describes the role.</span></span>

<span data-ttu-id="35c77-114">針對動畫控制項（例如複製檔案時顯示的動畫控制項），請使用 [**角色 \_ 系統 \_ 動畫**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="35c77-114">For animation controls, such as the animation control displayed when copying files, use [**ROLE\_SYSTEM\_ANIMATION**](object-roles.md).</span></span> <span data-ttu-id="35c77-115">偶爾動畫的圖形會描述為 [**角色 \_ 系統 \_ 圖形**](object-roles.md) ，其 [**狀態**](state-property.md) 屬性會設定為「 [**狀態 \_ 系統 \_ 動畫**](object-state-constants.md)」。</span><span class="sxs-lookup"><span data-stu-id="35c77-115">Graphics that are occasionally animated are described as [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md) with the [**State**](state-property.md) property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md).</span></span>

<span data-ttu-id="35c77-116">請注意，某些角色並不容易描述。</span><span class="sxs-lookup"><span data-stu-id="35c77-116">Note that some roles are not easy to describe.</span></span> <span data-ttu-id="35c77-117">例如，資料夾的大圖示視圖允許任意排列圖示，因此其角色可以描述為 [**角色 \_ 系統 \_ 群組**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="35c77-117">For example, a folder's large-icon view allows arbitrary arrangement of icons, so its role could be described as [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span> <span data-ttu-id="35c77-118">或者，提供固定資料列和資料行中之專案的控制項可能具有 [**角色 \_ 系統 \_ 資料表**](object-roles.md) 角色。</span><span class="sxs-lookup"><span data-stu-id="35c77-118">Or, a control that provides items in fixed rows and columns could have the [**ROLE\_SYSTEM\_TABLE**](object-roles.md) role.</span></span> <span data-ttu-id="35c77-119">因為角色是用來將使用模型傳達給終端使用者，所以請務必使用適當的角色。</span><span class="sxs-lookup"><span data-stu-id="35c77-119">Since a role is used to communicate the use model to an end user, it is important to use the appropriate role.</span></span> <span data-ttu-id="35c77-120">例如，如果您的控制項如同按鈕，則使用 [ [**角色 \_ 系統 \_**](object-roles.md)] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="35c77-120">For example, if your control acts like a button, then use [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md).</span></span>

 

 




