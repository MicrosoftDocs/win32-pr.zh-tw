---
description: 代表 CIE 的國際委員會 (電腦監視器的) 色彩特性。
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: WmiMonitorColorCharacteristics 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319579"
---
# <a name="wmimonitorcolorcharacteristics-class"></a><span data-ttu-id="f1baa-103">WmiMonitorColorCharacteristics 類別</span><span class="sxs-lookup"><span data-stu-id="f1baa-103">WmiMonitorColorCharacteristics class</span></span>

<span data-ttu-id="f1baa-104">**WmiMonitorColorCharacteristics** 類別代表照明上的國際委員會 (CIE 電腦監視器) 色彩特性。</span><span class="sxs-lookup"><span data-stu-id="f1baa-104">The **WmiMonitorColorCharacteristics** class represents the International Commission on Illumination (CIE) color characteristics of a computer monitor.</span></span> <span data-ttu-id="f1baa-105">資料對應至視頻電子產品標準關聯的 [色彩特性] 區塊中的資料 ([) 增強的擴充顯示器顯示識別資料 (E EDID) 結構。</span><span class="sxs-lookup"><span data-stu-id="f1baa-105">The data corresponds to data in the Color Characteristics block of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1baa-106">語法</span><span class="sxs-lookup"><span data-stu-id="f1baa-106">Syntax</span></span>

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a><span data-ttu-id="f1baa-107">成員</span><span class="sxs-lookup"><span data-stu-id="f1baa-107">Members</span></span>

<span data-ttu-id="f1baa-108">**WmiMonitorColorCharacteristics** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f1baa-108">The **WmiMonitorColorCharacteristics** class has these types of members:</span></span>

-   [<span data-ttu-id="f1baa-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f1baa-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1baa-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f1baa-110">Properties</span></span>

<span data-ttu-id="f1baa-111">**WmiMonitorColorCharacteristics** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f1baa-111">The **WmiMonitorColorCharacteristics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1baa-112">**使用中**</span><span class="sxs-lookup"><span data-stu-id="f1baa-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1baa-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f1baa-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1baa-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1baa-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1baa-115">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="f1baa-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="f1baa-116">**藍色**</span><span class="sxs-lookup"><span data-stu-id="f1baa-116">**Blue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1baa-117">資料類型： **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="f1baa-117">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f1baa-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1baa-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1baa-119">Blue 的 CIE 座標，由 [**XYZinCIE**](xyzincie.md) 類別的實例所表示。</span><span class="sxs-lookup"><span data-stu-id="f1baa-119">CIE coordinates for blue, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1baa-120">**DefaultWhite**</span><span class="sxs-lookup"><span data-stu-id="f1baa-120">**DefaultWhite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1baa-121">資料類型： **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="f1baa-121">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f1baa-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1baa-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1baa-123">預設的白色 CIE 座標。</span><span class="sxs-lookup"><span data-stu-id="f1baa-123">Default white CIE coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="f1baa-124">**綠色**</span><span class="sxs-lookup"><span data-stu-id="f1baa-124">**Green**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1baa-125">資料類型： **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="f1baa-125">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f1baa-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1baa-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1baa-127">CIE 以 [**XYZinCIE**](xyzincie.md) 類別的實例表示的綠色座標。</span><span class="sxs-lookup"><span data-stu-id="f1baa-127">CIE coordinates for green, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f1baa-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="f1baa-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1baa-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1baa-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1baa-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1baa-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1baa-131">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="f1baa-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f1baa-132">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1baa-132">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="f1baa-133">**紅色**</span><span class="sxs-lookup"><span data-stu-id="f1baa-133">**Red**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1baa-134">資料類型： **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="f1baa-134">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f1baa-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1baa-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1baa-136">CIE 的紅色座標，由 [**XYZinCIE**](xyzincie.md) 類別的實例所表示。</span><span class="sxs-lookup"><span data-stu-id="f1baa-136">CIE coordinates for red, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1baa-137">備註</span><span class="sxs-lookup"><span data-stu-id="f1baa-137">Remarks</span></span>

<span data-ttu-id="f1baa-138">Chromaticity 和白色點值會使用編碼格式來表示為小數數位。</span><span class="sxs-lookup"><span data-stu-id="f1baa-138">The chromaticity and white point values are expressed as fractional numbers using an encoding format.</span></span> <span data-ttu-id="f1baa-139">此格式精確到千位位置（長度為10個位）。</span><span class="sxs-lookup"><span data-stu-id="f1baa-139">This format is accurate to the thousandth place, which is 10 bits in length.</span></span> <span data-ttu-id="f1baa-140">最重要的位 (MSB) 代表 2 ^-1 和最不重要的位 (LSB) 分別代表 2 ^-10 個係數。</span><span class="sxs-lookup"><span data-stu-id="f1baa-140">The most significant bit (MSB) represents 2^-1 and the least significant bit (LSB) represents 2^-10 coefficients, respectively.</span></span> <span data-ttu-id="f1baa-141">電子 EDID v1. x 結構中儲存值的有效位數應精確為實際值的 +/-0.005。</span><span class="sxs-lookup"><span data-stu-id="f1baa-141">Precision of the stored values in the E-EDID v1.x structure should be accurate to +/- 0.005 of the actual value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1baa-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1baa-142">Requirements</span></span>



| <span data-ttu-id="f1baa-143">需求</span><span class="sxs-lookup"><span data-stu-id="f1baa-143">Requirement</span></span> | <span data-ttu-id="f1baa-144">值</span><span class="sxs-lookup"><span data-stu-id="f1baa-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1baa-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1baa-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f1baa-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1baa-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f1baa-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1baa-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f1baa-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1baa-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f1baa-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="f1baa-149">Namespace</span></span><br/>                | <span data-ttu-id="f1baa-150">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="f1baa-150">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="f1baa-151">MOF</span><span class="sxs-lookup"><span data-stu-id="f1baa-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1baa-152"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1baa-152"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1baa-153">DLL</span><span class="sxs-lookup"><span data-stu-id="f1baa-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1baa-154"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1baa-154"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1baa-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1baa-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1baa-156">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="f1baa-156">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




