---
description: 包含的方法可取得視頻電子產品標準關聯之影片輸入定義的原始內容 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 1.x 標準128位元組資料區塊。
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: WmiMonitorDescriptorMethods 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987287"
---
# <a name="wmimonitordescriptormethods-class"></a><span data-ttu-id="70d6d-103">WmiMonitorDescriptorMethods 類別</span><span class="sxs-lookup"><span data-stu-id="70d6d-103">WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="70d6d-104">**WmiMonitorDescriptorMethods** WMI 類別包含的方法可取得視頻電子郵件標準關聯之影片輸入定義的原始內容 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 1.x 標準128位元組資料區塊。</span><span class="sxs-lookup"><span data-stu-id="70d6d-104">The **WmiMonitorDescriptorMethods** WMI class contains methods that obtain the raw content of Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x standard 128-byte data blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d6d-105">語法</span><span class="sxs-lookup"><span data-stu-id="70d6d-105">Syntax</span></span>

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="70d6d-106">成員</span><span class="sxs-lookup"><span data-stu-id="70d6d-106">Members</span></span>

<span data-ttu-id="70d6d-107">**WmiMonitorDescriptorMethods** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="70d6d-107">The **WmiMonitorDescriptorMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="70d6d-108">方法</span><span class="sxs-lookup"><span data-stu-id="70d6d-108">Methods</span></span>](#wmimonitordescriptormethods-class)
-   [<span data-ttu-id="70d6d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="70d6d-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="70d6d-110">方法</span><span class="sxs-lookup"><span data-stu-id="70d6d-110">Methods</span></span>

<span data-ttu-id="70d6d-111">**WmiMonitorDescriptorMethods** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="70d6d-111">The **WmiMonitorDescriptorMethods** class has these methods.</span></span>



| <span data-ttu-id="70d6d-112">方法</span><span class="sxs-lookup"><span data-stu-id="70d6d-112">Method</span></span>                                                                                           | <span data-ttu-id="70d6d-113">描述</span><span class="sxs-lookup"><span data-stu-id="70d6d-113">Description</span></span>                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="70d6d-114">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="70d6d-114">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | <span data-ttu-id="70d6d-115">存取指定的 EDID 1.x 描述元區塊的原始資料。</span><span class="sxs-lookup"><span data-stu-id="70d6d-115">Accesses the raw data for a specified EDID v.1.x descriptor block.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="70d6d-116">屬性</span><span class="sxs-lookup"><span data-stu-id="70d6d-116">Properties</span></span>

<span data-ttu-id="70d6d-117">**WmiMonitorDescriptorMethods** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="70d6d-117">The **WmiMonitorDescriptorMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70d6d-118">**使用中**</span><span class="sxs-lookup"><span data-stu-id="70d6d-118">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70d6d-119">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="70d6d-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70d6d-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="70d6d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70d6d-121">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="70d6d-121">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="70d6d-122">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="70d6d-122">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70d6d-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="70d6d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70d6d-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="70d6d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70d6d-125">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="70d6d-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="70d6d-126">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="70d6d-126">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70d6d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="70d6d-127">Requirements</span></span>



| <span data-ttu-id="70d6d-128">需求</span><span class="sxs-lookup"><span data-stu-id="70d6d-128">Requirement</span></span> | <span data-ttu-id="70d6d-129">值</span><span class="sxs-lookup"><span data-stu-id="70d6d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70d6d-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70d6d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="70d6d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70d6d-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="70d6d-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70d6d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="70d6d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70d6d-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="70d6d-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="70d6d-134">Namespace</span></span><br/>                | <span data-ttu-id="70d6d-135">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="70d6d-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="70d6d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="70d6d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70d6d-137"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="70d6d-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="70d6d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="70d6d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70d6d-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70d6d-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70d6d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70d6d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70d6d-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="70d6d-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




