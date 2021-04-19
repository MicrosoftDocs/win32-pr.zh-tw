---
description: Win32 \_ MethodParameterClass abstract、BASE WMI 類別會衍生任何定義為參數值容器的類別，這些值會傳遞給方法。
ms.assetid: 293fa378-432d-4e97-a8ab-8dc4917d5476
ms.tgt_platform: multiple
title: Win32_MethodParameterClass 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MethodParameterClass
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e791941df681b2e46c4de6f0714b1290baecfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970708"
---
# <a name="win32_methodparameterclass-class"></a><span data-ttu-id="dbe2a-103">Win32 \_ MethodParameterClass 類別</span><span class="sxs-lookup"><span data-stu-id="dbe2a-103">Win32\_MethodParameterClass class</span></span>

<span data-ttu-id="dbe2a-104">**Win32 \_ MethodParameterClass** Abstract、base [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會衍生任何定義為參數值容器的類別，這些值會傳遞給方法。</span><span class="sxs-lookup"><span data-stu-id="dbe2a-104">The **Win32\_MethodParameterClass** abstract, base [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) derives any class defined as a container of parameter values that will be passed to a method.</span></span> <span data-ttu-id="dbe2a-105">沒有本身的屬性，這個類別會做為分類節點。</span><span class="sxs-lookup"><span data-stu-id="dbe2a-105">Having no properties of its own, this class serves as a classification node.</span></span> <span data-ttu-id="dbe2a-106">[**CIM \_ PhysicalElement**](cim-physicalelement.md)就是一個類似的範例。</span><span class="sxs-lookup"><span data-stu-id="dbe2a-106">A similar example is [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span> <span data-ttu-id="dbe2a-107">從 **CIM \_ PhysicalElement** 衍生表示類別會描述實體，而不是邏輯實體。</span><span class="sxs-lookup"><span data-stu-id="dbe2a-107">Derivation from **CIM\_PhysicalElement** indicates that the class describes a physical rather than logical entity.</span></span> <span data-ttu-id="dbe2a-108">在 **Win32 \_ MethodParameterClass** 的情況下，會特別建立從中衍生的類別，以便將參數傳遞給方法。</span><span class="sxs-lookup"><span data-stu-id="dbe2a-108">In the case of **Win32\_MethodParameterClass**, classes derived from it are created specifically to pass parameters to a method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe2a-109">語法</span><span class="sxs-lookup"><span data-stu-id="dbe2a-109">Syntax</span></span>

## <a name="members"></a><span data-ttu-id="dbe2a-110">成員</span><span class="sxs-lookup"><span data-stu-id="dbe2a-110">Members</span></span>

<span data-ttu-id="dbe2a-111">**Win32 \_ MethodParameterClass** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="dbe2a-111">The **Win32\_MethodParameterClass** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe2a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbe2a-112">Requirements</span></span>



| <span data-ttu-id="dbe2a-113">需求</span><span class="sxs-lookup"><span data-stu-id="dbe2a-113">Requirement</span></span> | <span data-ttu-id="dbe2a-114">值</span><span class="sxs-lookup"><span data-stu-id="dbe2a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe2a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbe2a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe2a-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbe2a-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dbe2a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbe2a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe2a-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbe2a-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dbe2a-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="dbe2a-119">Namespace</span></span><br/>                | <span data-ttu-id="dbe2a-120">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dbe2a-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dbe2a-121">MOF</span><span class="sxs-lookup"><span data-stu-id="dbe2a-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbe2a-122"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbe2a-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbe2a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="dbe2a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbe2a-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbe2a-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe2a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbe2a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe2a-126">WMI 服務管理類別</span><span class="sxs-lookup"><span data-stu-id="dbe2a-126">WMI Service Management Classes</span></span>](/windows/desktop/CIMWin32Prov/wmi-service-management-classes)
</dt> </dl>

 

