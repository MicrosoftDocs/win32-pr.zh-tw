---
description: 將影片標頭與包含該視訊卡的視訊卡產生關聯。
ms.assetid: d15f4350-1529-4246-9ea2-8453e52516c6
title: CIM_VideoHeadOnController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHeadOnController
- CIM_VideoHeadOnController.Antecedent
- CIM_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18178e6d9d7f1e684af1d4fe74336e1f2a02eedc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000271"
---
# <a name="cim_videoheadoncontroller-class"></a><span data-ttu-id="93b14-103">CIM \_ VideoHeadOnController 類別</span><span class="sxs-lookup"><span data-stu-id="93b14-103">CIM\_VideoHeadOnController class</span></span>

<span data-ttu-id="93b14-104">將影片標頭與包含該視訊卡的視訊卡產生關聯。</span><span class="sxs-lookup"><span data-stu-id="93b14-104">Associates a video head with the video adapter that contains it.</span></span>

## <a name="syntax"></a><span data-ttu-id="93b14-105">語法</span><span class="sxs-lookup"><span data-stu-id="93b14-105">Syntax</span></span>

``` syntax
[Association, Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHeadOnController : CIM_HostedDependency
{
  CIM_DisplayController REF Antecedent;
  CIM_VideoHead         REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="93b14-106">成員</span><span class="sxs-lookup"><span data-stu-id="93b14-106">Members</span></span>

<span data-ttu-id="93b14-107">**CIM \_ VideoHeadOnController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="93b14-107">The **CIM\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="93b14-108">屬性</span><span class="sxs-lookup"><span data-stu-id="93b14-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93b14-109">屬性</span><span class="sxs-lookup"><span data-stu-id="93b14-109">Properties</span></span>

<span data-ttu-id="93b14-110">**CIM \_ VideoHeadOnController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="93b14-110">The **CIM\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93b14-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="93b14-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93b14-112">資料類型： **CIM \_ DisplayController**</span><span class="sxs-lookup"><span data-stu-id="93b14-112">Data type: **CIM\_DisplayController**</span></span>
</dt> <dt>

<span data-ttu-id="93b14-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93b14-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93b14-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="93b14-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="93b14-115">包含 head 的視訊卡。</span><span class="sxs-lookup"><span data-stu-id="93b14-115">The video adapter that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="93b14-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="93b14-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93b14-117">資料類型： **CIM \_ VideoHead**</span><span class="sxs-lookup"><span data-stu-id="93b14-117">Data type: **CIM\_VideoHead**</span></span>
</dt> <dt>

<span data-ttu-id="93b14-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93b14-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93b14-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) ， [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="93b14-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="93b14-120">視訊卡上的標頭。</span><span class="sxs-lookup"><span data-stu-id="93b14-120">The head on the video adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93b14-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="93b14-121">Requirements</span></span>



| <span data-ttu-id="93b14-122">需求</span><span class="sxs-lookup"><span data-stu-id="93b14-122">Requirement</span></span> | <span data-ttu-id="93b14-123">值</span><span class="sxs-lookup"><span data-stu-id="93b14-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93b14-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93b14-124">Minimum supported client</span></span><br/> | <span data-ttu-id="93b14-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="93b14-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="93b14-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93b14-126">Minimum supported server</span></span><br/> | <span data-ttu-id="93b14-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93b14-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="93b14-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="93b14-128">Namespace</span></span><br/>                | <span data-ttu-id="93b14-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="93b14-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="93b14-130">MOF</span><span class="sxs-lookup"><span data-stu-id="93b14-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93b14-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="93b14-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93b14-132">DLL</span><span class="sxs-lookup"><span data-stu-id="93b14-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93b14-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93b14-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93b14-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93b14-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93b14-135">**CIM \_ HostedDependency**</span><span class="sxs-lookup"><span data-stu-id="93b14-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

