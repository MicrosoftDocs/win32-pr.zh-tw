---
description: 從中衍生所有機器檢查架構 (MCA) 提供者資料類別（例如 MSMCAInfo RawMCAData）的抽象基類 \_ 。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: MSMCAInfo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026206"
---
# <a name="msmcainfo-class"></a><span data-ttu-id="b9173-104">MSMCAInfo 類別</span><span class="sxs-lookup"><span data-stu-id="b9173-104">MSMCAInfo class</span></span>

<span data-ttu-id="b9173-105">**MSMCAInfo** 類別是一個抽象基類，所有機器檢查架構 (MCA) 提供者資料類別（例如 [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md)）都會衍生。</span><span class="sxs-lookup"><span data-stu-id="b9173-105">The **MSMCAInfo** class is an abstract base class from which all Machine Check Architecture (MCA) provider data classes, such as [**MSMCAInfo\_RawMCAData**](msmcainfo-rawmcadata.md), are derived.</span></span> <span data-ttu-id="b9173-106">MCA 提供者也有衍生自 [**>register-wmievent**](wmievent.md)的事件類別。</span><span class="sxs-lookup"><span data-stu-id="b9173-106">The MCA provider also has event classes, derived from [**WMIEvent**](wmievent.md).</span></span> <span data-ttu-id="b9173-107">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="b9173-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="b9173-108">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b9173-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b9173-109">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="b9173-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9173-110">語法</span><span class="sxs-lookup"><span data-stu-id="b9173-110">Syntax</span></span>

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a><span data-ttu-id="b9173-111">成員</span><span class="sxs-lookup"><span data-stu-id="b9173-111">Members</span></span>

<span data-ttu-id="b9173-112">**MSMCAInfo** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="b9173-112">The **MSMCAInfo** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9173-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9173-113">Requirements</span></span>



| <span data-ttu-id="b9173-114">需求</span><span class="sxs-lookup"><span data-stu-id="b9173-114">Requirement</span></span> | <span data-ttu-id="b9173-115">值</span><span class="sxs-lookup"><span data-stu-id="b9173-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9173-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9173-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b9173-117">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b9173-117">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="b9173-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9173-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b9173-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b9173-119">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="b9173-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="b9173-120">Namespace</span></span><br/>                | <span data-ttu-id="b9173-121">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="b9173-121">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b9173-122">MOF</span><span class="sxs-lookup"><span data-stu-id="b9173-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9173-123"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9173-123"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9173-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b9173-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9173-125"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9173-125"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9173-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9173-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9173-127">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="b9173-127">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="b9173-128">**MSMCAEvent \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="b9173-128">**MSMCAEvent\_Header**</span></span>](msmcaevent-header.md)
</dt> <dt>

[<span data-ttu-id="b9173-129">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="b9173-129">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




