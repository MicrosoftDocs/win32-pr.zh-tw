---
description: 包含在照明上的國際委員會 (CIE) XYZ 色彩空間顯示的座標。
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: XYZinCIE 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992081"
---
# <a name="xyzincie-class"></a><span data-ttu-id="cc8e5-103">XYZinCIE 類別</span><span class="sxs-lookup"><span data-stu-id="cc8e5-103">XYZinCIE class</span></span>

<span data-ttu-id="cc8e5-104">**XYZinCIE** WMI 類別包含在照明 (CIE) XYZ 色彩空間的國際委員會顯示器座標。</span><span class="sxs-lookup"><span data-stu-id="cc8e5-104">The **XYZinCIE** WMI class contains the coordinates of the display in the International Commission on Illumination (CIE) XYZ color space.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc8e5-105">語法</span><span class="sxs-lookup"><span data-stu-id="cc8e5-105">Syntax</span></span>

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a><span data-ttu-id="cc8e5-106">成員</span><span class="sxs-lookup"><span data-stu-id="cc8e5-106">Members</span></span>

<span data-ttu-id="cc8e5-107">**XYZinCIE** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cc8e5-107">The **XYZinCIE** class has these types of members:</span></span>

-   [<span data-ttu-id="cc8e5-108">屬性</span><span class="sxs-lookup"><span data-stu-id="cc8e5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc8e5-109">屬性</span><span class="sxs-lookup"><span data-stu-id="cc8e5-109">Properties</span></span>

<span data-ttu-id="cc8e5-110">**XYZinCIE** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cc8e5-110">The **XYZinCIE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc8e5-111">**X**</span><span class="sxs-lookup"><span data-stu-id="cc8e5-111">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc8e5-112">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cc8e5-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc8e5-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cc8e5-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc8e5-114">X 座標。</span><span class="sxs-lookup"><span data-stu-id="cc8e5-114">X-coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cc8e5-115">**Y**</span><span class="sxs-lookup"><span data-stu-id="cc8e5-115">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc8e5-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cc8e5-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc8e5-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cc8e5-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc8e5-118">Y 座標。</span><span class="sxs-lookup"><span data-stu-id="cc8e5-118">Y-coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc8e5-119">備註</span><span class="sxs-lookup"><span data-stu-id="cc8e5-119">Remarks</span></span>

<span data-ttu-id="cc8e5-120">[**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md)類別包含 **XYZinCIE** 類別的內嵌實例，用以描述監視的色彩特性。</span><span class="sxs-lookup"><span data-stu-id="cc8e5-120">The [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) class contains embedded instances of the **XYZinCIE** class to describe the color characteristics of a monitor.</span></span>

<span data-ttu-id="cc8e5-121">若要根據 x 和 y 值計算 z 座標，請使用 \| \| (x，y，z) \| \| = 1 的關聯性。</span><span class="sxs-lookup"><span data-stu-id="cc8e5-121">To calculate the z-coordinate, based on the x and y values, use the relation \|\|(x,y,z)\|\| = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc8e5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc8e5-122">Requirements</span></span>



| <span data-ttu-id="cc8e5-123">需求</span><span class="sxs-lookup"><span data-stu-id="cc8e5-123">Requirement</span></span> | <span data-ttu-id="cc8e5-124">值</span><span class="sxs-lookup"><span data-stu-id="cc8e5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8e5-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc8e5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cc8e5-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc8e5-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cc8e5-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc8e5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cc8e5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc8e5-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cc8e5-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="cc8e5-129">Namespace</span></span><br/>                | <span data-ttu-id="cc8e5-130">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="cc8e5-130">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="cc8e5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cc8e5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc8e5-132"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e5-132"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc8e5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cc8e5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc8e5-134"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e5-134"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc8e5-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc8e5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc8e5-136">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="cc8e5-136">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




