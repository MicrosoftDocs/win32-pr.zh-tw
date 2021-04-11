---
description: 將影片標頭與包含它的影片控制器產生關聯。
ms.assetid: D072DF7C-D55B-4203-9FE5-B395D1EC1632
title: Msvm_VideoHeadOnController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHeadOnController
- Msvm_VideoHeadOnController.Antecedent
- Msvm_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11065c7b7a9e23b786697c3d4f0dbd63e67d6b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115404"
---
# <a name="msvm_videoheadoncontroller-class"></a><span data-ttu-id="b5a6a-103">Msvm \_ VideoHeadOnController 類別</span><span class="sxs-lookup"><span data-stu-id="b5a6a-103">Msvm\_VideoHeadOnController class</span></span>

<span data-ttu-id="b5a6a-104">將影片標頭與包含它的影片控制器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b5a6a-104">Associates a video head with the video controller that includes it.</span></span>

<span data-ttu-id="b5a6a-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b5a6a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a6a-106">語法</span><span class="sxs-lookup"><span data-stu-id="b5a6a-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHeadOnController : CIM_VideoHeadOnController
{
  CIM_DisplayController REF Antecedent;
  Msvm_VideoHead        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b5a6a-107">成員</span><span class="sxs-lookup"><span data-stu-id="b5a6a-107">Members</span></span>

<span data-ttu-id="b5a6a-108">**Msvm \_ VideoHeadOnController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b5a6a-108">The **Msvm\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="b5a6a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b5a6a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5a6a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b5a6a-110">Properties</span></span>

<span data-ttu-id="b5a6a-111">**Msvm \_ VideoHeadOnController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b5a6a-111">The **Msvm\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5a6a-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="b5a6a-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a6a-113">資料類型： **[ **CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b5a6a-113">Data type: **[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="b5a6a-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a6a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a6a-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="b5a6a-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b5a6a-116">包含 head 的影片控制器。</span><span class="sxs-lookup"><span data-stu-id="b5a6a-116">The video controller that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="b5a6a-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="b5a6a-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a6a-118">資料類型： **[ **Msvm \_ VideoHead**](msvm-videohead.md)**</span><span class="sxs-lookup"><span data-stu-id="b5a6a-118">Data type: **[**Msvm\_VideoHead**](msvm-videohead.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b5a6a-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b5a6a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a6a-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) ， [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="b5a6a-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b5a6a-121">影片裝置上的標頭。</span><span class="sxs-lookup"><span data-stu-id="b5a6a-121">The head on the video device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5a6a-122">備註</span><span class="sxs-lookup"><span data-stu-id="b5a6a-122">Remarks</span></span>

<span data-ttu-id="b5a6a-123">存取 **Msvm \_ VideoHeadOnController** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="b5a6a-123">Access to the **Msvm\_VideoHeadOnController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b5a6a-124">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="b5a6a-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a6a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5a6a-125">Requirements</span></span>



| <span data-ttu-id="b5a6a-126">需求</span><span class="sxs-lookup"><span data-stu-id="b5a6a-126">Requirement</span></span> | <span data-ttu-id="b5a6a-127">值</span><span class="sxs-lookup"><span data-stu-id="b5a6a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a6a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5a6a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a6a-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5a6a-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b5a6a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5a6a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a6a-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5a6a-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5a6a-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="b5a6a-132">Namespace</span></span><br/>                | <span data-ttu-id="b5a6a-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b5a6a-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b5a6a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b5a6a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5a6a-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b5a6a-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5a6a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b5a6a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5a6a-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5a6a-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5a6a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5a6a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a6a-139">**CIM \_ VideoHeadOnController**</span><span class="sxs-lookup"><span data-stu-id="b5a6a-139">**CIM\_VideoHeadOnController**</span></span>](cim-videoheadoncontroller.md)
</dt> <dt>

<span data-ttu-id="b5a6a-140">[**CIM \_ VideoHeadOnController**](/previous-versions//cc136950(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b5a6a-140">[**CIM\_VideoHeadOnController**](/previous-versions//cc136950(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b5a6a-141">影片類別</span><span class="sxs-lookup"><span data-stu-id="b5a6a-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

