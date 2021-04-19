---
description: 唯讀 ComponentClients 屬性會傳回 StringList 物件，以列舉指定元件的一組用戶端。
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: ComponentClients 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998410"
---
# <a name="installercomponentclients-property"></a><span data-ttu-id="ced91-103">ComponentClients 屬性</span><span class="sxs-lookup"><span data-stu-id="ced91-103">Installer.ComponentClients property</span></span>

<span data-ttu-id="ced91-104">唯讀 **ComponentClients** 屬性會傳回 [**StringList**](stringlist-object.md) 物件，以列舉指定元件的一組用戶端。</span><span class="sxs-lookup"><span data-stu-id="ced91-104">The read-only **ComponentClients** property returns a [**StringList**](stringlist-object.md) object enumerating the set of clients of a specified component.</span></span>

<span data-ttu-id="ced91-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ced91-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ced91-106">語法</span><span class="sxs-lookup"><span data-stu-id="ced91-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a><span data-ttu-id="ced91-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="ced91-107">Property value</span></span>

<span data-ttu-id="ced91-108">字串 GUID，表示元件的元件代碼。</span><span class="sxs-lookup"><span data-stu-id="ced91-108">A string GUID that represents the component code of the component.</span></span> <span data-ttu-id="ced91-109">元件程式碼會在 [元件資料表](component-table.md)的 [元件] 資料行中指定。</span><span class="sxs-lookup"><span data-stu-id="ced91-109">The component codes are specified in the ComponentId column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ced91-110">備註</span><span class="sxs-lookup"><span data-stu-id="ced91-110">Remarks</span></span>

<span data-ttu-id="ced91-111">若要列舉元件用戶端，應用程式可以使用 For Each 結構來逐一查看 [**StringList**](stringlist-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ced91-111">To enumerate the component clients, an application may iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="ced91-112">因為不會排序用戶端，所以任何新元件都有任意的索引。</span><span class="sxs-lookup"><span data-stu-id="ced91-112">Because clients are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="ced91-113">這表示函數可能會以任何順序傳回用戶端。</span><span class="sxs-lookup"><span data-stu-id="ced91-113">This means that the function may return clients in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="ced91-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ced91-114">Requirements</span></span>



| <span data-ttu-id="ced91-115">需求</span><span class="sxs-lookup"><span data-stu-id="ced91-115">Requirement</span></span> | <span data-ttu-id="ced91-116">值</span><span class="sxs-lookup"><span data-stu-id="ced91-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ced91-117">版本</span><span class="sxs-lookup"><span data-stu-id="ced91-117">Version</span></span><br/> | <span data-ttu-id="ced91-118">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="ced91-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ced91-119">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="ced91-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ced91-120">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ced91-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ced91-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ced91-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="ced91-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ced91-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ced91-123">IID</span><span class="sxs-lookup"><span data-stu-id="ced91-123">IID</span></span><br/>     | <span data-ttu-id="ced91-124">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ced91-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="ced91-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ced91-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ced91-126">**MsiEnumClients**</span><span class="sxs-lookup"><span data-stu-id="ced91-126">**MsiEnumClients**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




