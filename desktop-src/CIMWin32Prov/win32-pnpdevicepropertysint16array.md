---
description: 代表由 Sint16 元素陣列組成的 PnP 裝置屬性。
ms.assetid: 0A445D60-3E37-4E9E-BD71-2FEECB4BC440
ms.tgt_platform: multiple
title: Win32_PnPDevicePropertySint16Array 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevicePropertySint16Array
- Win32_PnPDevicePropertySint16Array.Key
- Win32_PnPDevicePropertySint16Array.KeyName
- Win32_PnPDevicePropertySint16Array.Type
- Win32_PnPDevicePropertySint16Array.DeviceID
- Win32_PnPDevicePropertySint16Array.Data
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 282b15a1a936834d283eb9577e503d650ebe1dd3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111580"
---
# <a name="win32_pnpdevicepropertysint16array-class"></a><span data-ttu-id="bb885-103">Win32 \_ PnPDevicePropertySint16Array 類別</span><span class="sxs-lookup"><span data-stu-id="bb885-103">Win32\_PnPDevicePropertySint16Array class</span></span>

<span data-ttu-id="bb885-104">代表由 **Sint16** 元素陣列組成的 PnP 裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="bb885-104">Represents a PnP device property consisting of an array of **Sint16** elements.</span></span>

<span data-ttu-id="bb885-105">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bb885-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb885-106">語法</span><span class="sxs-lookup"><span data-stu-id="bb885-106">Syntax</span></span>

``` syntax
class Win32_PnPDevicePropertySint16Array : Win32_PnPDeviceProperty
{
  string Key;
  string KeyName;
  Uint32 Type;
  string DeviceID;
  Sint16 Data[];
};
```

## <a name="members"></a><span data-ttu-id="bb885-107">成員</span><span class="sxs-lookup"><span data-stu-id="bb885-107">Members</span></span>

<span data-ttu-id="bb885-108">**Win32 \_ PnPDevicePropertySint16Array** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bb885-108">The **Win32\_PnPDevicePropertySint16Array** class has these types of members:</span></span>

-   [<span data-ttu-id="bb885-109">屬性</span><span class="sxs-lookup"><span data-stu-id="bb885-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb885-110">屬性</span><span class="sxs-lookup"><span data-stu-id="bb885-110">Properties</span></span>

<span data-ttu-id="bb885-111">**Win32 \_ PnPDevicePropertySint16Array** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bb885-111">The **Win32\_PnPDevicePropertySint16Array** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb885-112">**資料**</span><span class="sxs-lookup"><span data-stu-id="bb885-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb885-113">資料類型： **Sint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bb885-113">Data type: **Sint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bb885-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bb885-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb885-115">屬性值。</span><span class="sxs-lookup"><span data-stu-id="bb885-115">The property value.</span></span>

</dd> <dt>

<span data-ttu-id="bb885-116">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="bb885-116">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb885-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bb885-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb885-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bb885-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb885-119">識別 PnP 裝置。</span><span class="sxs-lookup"><span data-stu-id="bb885-119">Identifies the PnP device.</span></span>

<span data-ttu-id="bb885-120">這個屬性繼承自 [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md)。</span><span class="sxs-lookup"><span data-stu-id="bb885-120">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb885-121">**金鑰**</span><span class="sxs-lookup"><span data-stu-id="bb885-121">**Key**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb885-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bb885-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb885-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bb885-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb885-124">識別 **資料** 屬性之索引鍵 Name-Value 組的值。</span><span class="sxs-lookup"><span data-stu-id="bb885-124">The value of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="bb885-125">這個屬性繼承自 [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md)。</span><span class="sxs-lookup"><span data-stu-id="bb885-125">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb885-126">**KeyName**</span><span class="sxs-lookup"><span data-stu-id="bb885-126">**KeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb885-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bb885-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb885-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bb885-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb885-129">識別 **資料** 屬性之索引鍵 Name-Value 組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb885-129">The name of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="bb885-130">這個屬性繼承自 [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md)。</span><span class="sxs-lookup"><span data-stu-id="bb885-130">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb885-131">**型別**</span><span class="sxs-lookup"><span data-stu-id="bb885-131">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb885-132">資料類型： **Uint32**</span><span class="sxs-lookup"><span data-stu-id="bb885-132">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb885-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bb885-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb885-134">**資料** 屬性的型別。</span><span class="sxs-lookup"><span data-stu-id="bb885-134">The type of the **Data** property.</span></span>

<span data-ttu-id="bb885-135">這個屬性繼承自 [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md)。</span><span class="sxs-lookup"><span data-stu-id="bb885-135">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

<span data-ttu-id="bb885-136">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="bb885-136">The possible values are.</span></span>

<dt>

<span id="Empty"></span><span id="empty"></span><span id="EMPTY"></span>

<span data-ttu-id="bb885-137">**空白** (0) </span><span class="sxs-lookup"><span data-stu-id="bb885-137">**Empty** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Null"></span><span id="null"></span><span id="NULL"></span>

<span data-ttu-id="bb885-138">**Null** (1) </span><span class="sxs-lookup"><span data-stu-id="bb885-138">**Null** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SByte"></span><span id="sbyte"></span><span id="SBYTE"></span>

<span data-ttu-id="bb885-139">**SByte** (2) </span><span class="sxs-lookup"><span data-stu-id="bb885-139">**SByte** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Byte"></span><span id="byte"></span><span id="BYTE"></span>

<span data-ttu-id="bb885-140">**Byte** (3) </span><span class="sxs-lookup"><span data-stu-id="bb885-140">**Byte** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16"></span><span id="int16"></span><span id="INT16"></span>

<span data-ttu-id="bb885-141">**Int16** (4) </span><span class="sxs-lookup"><span data-stu-id="bb885-141">**Int16** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16"></span><span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="bb885-142">**UInt16** (5) </span><span class="sxs-lookup"><span data-stu-id="bb885-142">**UInt16** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Int32"></span><span id="int32"></span><span id="INT32"></span>

<span data-ttu-id="bb885-143">**Int32** (6) </span><span class="sxs-lookup"><span data-stu-id="bb885-143">**Int32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Uint32"></span><span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="bb885-144">**Uint32** (7) </span><span class="sxs-lookup"><span data-stu-id="bb885-144">**Uint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64"></span><span id="int64"></span><span id="INT64"></span>

<span data-ttu-id="bb885-145">**Int64** (8) </span><span class="sxs-lookup"><span data-stu-id="bb885-145">**Int64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64"></span><span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="bb885-146">**UInt64** (9) </span><span class="sxs-lookup"><span data-stu-id="bb885-146">**UInt64** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Float"></span><span id="float"></span><span id="FLOAT"></span>

<span data-ttu-id="bb885-147">**Float** (10) </span><span class="sxs-lookup"><span data-stu-id="bb885-147">**Float** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Double"></span><span id="double"></span><span id="DOUBLE"></span>

<span data-ttu-id="bb885-148">**Double** (11) </span><span class="sxs-lookup"><span data-stu-id="bb885-148">**Double** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Decimal"></span><span id="decimal"></span><span id="DECIMAL"></span>

<span data-ttu-id="bb885-149">**Decimal** (12) </span><span class="sxs-lookup"><span data-stu-id="bb885-149">**Decimal** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Guid"></span><span id="guid"></span><span id="GUID"></span>

<span data-ttu-id="bb885-150">**Guid** (13) </span><span class="sxs-lookup"><span data-stu-id="bb885-150">**Guid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Currency"></span><span id="currency"></span><span id="CURRENCY"></span>

<span data-ttu-id="bb885-151">**Currency** (14) </span><span class="sxs-lookup"><span data-stu-id="bb885-151">**Currency** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Date"></span><span id="date"></span><span id="DATE"></span>

<span data-ttu-id="bb885-152">**日期** (15) </span><span class="sxs-lookup"><span data-stu-id="bb885-152">**Date** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTime"></span><span id="filetime"></span><span id="FILETIME"></span>

<span data-ttu-id="bb885-153">**FileTime** (16) </span><span class="sxs-lookup"><span data-stu-id="bb885-153">**FileTime** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="bb885-154">**布林值** (17) </span><span class="sxs-lookup"><span data-stu-id="bb885-154">**Boolean** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="String"></span><span id="string"></span><span id="STRING"></span>

<span data-ttu-id="bb885-155">**字串** (18) </span><span class="sxs-lookup"><span data-stu-id="bb885-155">**String** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptor"></span><span id="securitydescriptor"></span><span id="SECURITYDESCRIPTOR"></span>

<span data-ttu-id="bb885-156">**SecurityDescriptor** (19) </span><span class="sxs-lookup"><span data-stu-id="bb885-156">**SecurityDescriptor** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorString"></span><span id="securitydescriptorstring"></span><span id="SECURITYDESCRIPTORSTRING"></span>

<span data-ttu-id="bb885-157">**SecurityDescriptorString** (20) </span><span class="sxs-lookup"><span data-stu-id="bb885-157">**SecurityDescriptorString** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEY"></span><span id="devpropkey"></span>

<span data-ttu-id="bb885-158">**DEVPROPKEY** (21) </span><span class="sxs-lookup"><span data-stu-id="bb885-158">**DEVPROPKEY** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPE"></span><span id="devproptype"></span>

<span data-ttu-id="bb885-159">**DEVPROPTYPE** (22) </span><span class="sxs-lookup"><span data-stu-id="bb885-159">**DEVPROPTYPE** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bb885-160">**錯誤** (23) </span><span class="sxs-lookup"><span data-stu-id="bb885-160">**Error** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatus"></span><span id="ntstatus"></span><span id="NTSTATUS"></span>

<span data-ttu-id="bb885-161"> (24) 的 **NTStatus**</span><span class="sxs-lookup"><span data-stu-id="bb885-161">**NTStatus** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirect"></span><span id="stringindirect"></span><span id="STRINGINDIRECT"></span>

<span data-ttu-id="bb885-162">**StringIndirect** (25) </span><span class="sxs-lookup"><span data-stu-id="bb885-162">**StringIndirect** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="bb885-163">**已保留**</span><span class="sxs-lookup"><span data-stu-id="bb885-163">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="bb885-164">26–4097</span><span class="sxs-lookup"><span data-stu-id="bb885-164">26–4097</span></span></dd> <dt>

<span id="SByteArray"></span><span id="sbytearray"></span><span id="SBYTEARRAY"></span>

<span data-ttu-id="bb885-165">**SByteArray** (4098) </span><span class="sxs-lookup"><span data-stu-id="bb885-165">**SByteArray** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="bb885-166">**Binary** (4099) </span><span class="sxs-lookup"><span data-stu-id="bb885-166">**Binary** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16Array"></span><span id="int16array"></span><span id="INT16ARRAY"></span>

<span data-ttu-id="bb885-167">**Int16Array** (4100) </span><span class="sxs-lookup"><span data-stu-id="bb885-167">**Int16Array** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16Array"></span><span id="uint16array"></span><span id="UINT16ARRAY"></span>

<span data-ttu-id="bb885-168">**UInt16Array** (4101) </span><span class="sxs-lookup"><span data-stu-id="bb885-168">**UInt16Array** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64Array"></span><span id="int64array"></span><span id="INT64ARRAY"></span>

<span data-ttu-id="bb885-169">**Int64Array** (4102) </span><span class="sxs-lookup"><span data-stu-id="bb885-169">**Int64Array** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64Array"></span><span id="uint64array"></span><span id="UINT64ARRAY"></span>

<span data-ttu-id="bb885-170">**UInt64Array** (4103) </span><span class="sxs-lookup"><span data-stu-id="bb885-170">**UInt64Array** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="FloatArray"></span><span id="floatarray"></span><span id="FLOATARRAY"></span>

<span data-ttu-id="bb885-171">**FloatArray** (4104) </span><span class="sxs-lookup"><span data-stu-id="bb885-171">**FloatArray** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="DoubleArray"></span><span id="doublearray"></span><span id="DOUBLEARRAY"></span>

<span data-ttu-id="bb885-172">**DoubleArray** (4105) </span><span class="sxs-lookup"><span data-stu-id="bb885-172">**DoubleArray** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="DecimalArray"></span><span id="decimalarray"></span><span id="DECIMALARRAY"></span>

<span data-ttu-id="bb885-173">**DecimalArray** (4106) </span><span class="sxs-lookup"><span data-stu-id="bb885-173">**DecimalArray** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="GuidArray"></span><span id="guidarray"></span><span id="GUIDARRAY"></span>

<span data-ttu-id="bb885-174">**GuidArray** (4107) </span><span class="sxs-lookup"><span data-stu-id="bb885-174">**GuidArray** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="CurrencyArray"></span><span id="currencyarray"></span><span id="CURRENCYARRAY"></span>

<span data-ttu-id="bb885-175">**CurrencyArray** (4108) </span><span class="sxs-lookup"><span data-stu-id="bb885-175">**CurrencyArray** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="DateArray"></span><span id="datearray"></span><span id="DATEARRAY"></span>

<span data-ttu-id="bb885-176">**DateArray** (4109) </span><span class="sxs-lookup"><span data-stu-id="bb885-176">**DateArray** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTimeArray"></span><span id="filetimearray"></span><span id="FILETIMEARRAY"></span>

<span data-ttu-id="bb885-177">**FileTimeArray** (4110) </span><span class="sxs-lookup"><span data-stu-id="bb885-177">**FileTimeArray** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="BooleanArray"></span><span id="booleanarray"></span><span id="BOOLEANARRAY"></span>

<span data-ttu-id="bb885-178">**BooleanArray** (4111) </span><span class="sxs-lookup"><span data-stu-id="bb885-178">**BooleanArray** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="StringList"></span><span id="stringlist"></span><span id="STRINGLIST"></span>

<span data-ttu-id="bb885-179">**StringList** (4112) </span><span class="sxs-lookup"><span data-stu-id="bb885-179">**StringList** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorList"></span><span id="securitydescriptorlist"></span><span id="SECURITYDESCRIPTORLIST"></span>

<span data-ttu-id="bb885-180">**SecurityDescriptorList** (4113) </span><span class="sxs-lookup"><span data-stu-id="bb885-180">**SecurityDescriptorList** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorStringList"></span><span id="securitydescriptorstringlist"></span><span id="SECURITYDESCRIPTORSTRINGLIST"></span>

<span data-ttu-id="bb885-181">**SecurityDescriptorStringList** (8210) </span><span class="sxs-lookup"><span data-stu-id="bb885-181">**SecurityDescriptorStringList** (8210)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEYArray"></span><span id="devpropkeyarray"></span><span id="DEVPROPKEYARRAY"></span>

<span data-ttu-id="bb885-182">**DEVPROPKEYArray** (8211) </span><span class="sxs-lookup"><span data-stu-id="bb885-182">**DEVPROPKEYArray** (8211)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPEArray"></span><span id="devproptypearray"></span><span id="DEVPROPTYPEARRAY"></span>

<span data-ttu-id="bb885-183">**DEVPROPTYPEArray** (8212) </span><span class="sxs-lookup"><span data-stu-id="bb885-183">**DEVPROPTYPEArray** (8212)</span></span>


</dt> <dd></dd> <dt>

<span id="ErrorArray"></span><span id="errorarray"></span><span id="ERRORARRAY"></span>

<span data-ttu-id="bb885-184">**ErrorArray** (4117) </span><span class="sxs-lookup"><span data-stu-id="bb885-184">**ErrorArray** (4117)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatusArray"></span><span id="ntstatusarray"></span><span id="NTSTATUSARRAY"></span>

<span data-ttu-id="bb885-185">**NTStatusArray** (4118) </span><span class="sxs-lookup"><span data-stu-id="bb885-185">**NTStatusArray** (4118)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirectList"></span><span id="stringindirectlist"></span><span id="STRINGINDIRECTLIST"></span>

<span data-ttu-id="bb885-186">**StringIndirectList** (4119) </span><span class="sxs-lookup"><span data-stu-id="bb885-186">**StringIndirectList** (4119)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_-_check_in_devpropdef.h"></span><span id="unknown_-_check_in_devpropdef.h"></span><span id="UNKNOWN_-_CHECK_IN_DEVPROPDEF.H"></span>

<span data-ttu-id="bb885-187">**未知-在 devpropdef 中檢查** (4120) </span><span class="sxs-lookup"><span data-stu-id="bb885-187">**Unknown - check in devpropdef.h** (4120)</span></span>


</dt> <dd></dd> <dt>

<span id="TBD"></span><span id="tbd"></span>

<span data-ttu-id="bb885-188">**TBD** (8217) </span><span class="sxs-lookup"><span data-stu-id="bb885-188">**TBD** (8217)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="bb885-189">**已保留**</span><span class="sxs-lookup"><span data-stu-id="bb885-189">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="bb885-190">8218–4294967295</span><span class="sxs-lookup"><span data-stu-id="bb885-190">8218–4294967295</span></span></dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb885-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb885-191">Requirements</span></span>



| <span data-ttu-id="bb885-192">需求</span><span class="sxs-lookup"><span data-stu-id="bb885-192">Requirement</span></span> | <span data-ttu-id="bb885-193">值</span><span class="sxs-lookup"><span data-stu-id="bb885-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb885-194">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb885-194">Minimum supported client</span></span><br/> | <span data-ttu-id="bb885-195">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb885-195">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bb885-196">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb885-196">Minimum supported server</span></span><br/> | <span data-ttu-id="bb885-197">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bb885-197">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="bb885-198">命名空間</span><span class="sxs-lookup"><span data-stu-id="bb885-198">Namespace</span></span><br/>                | <span data-ttu-id="bb885-199">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bb885-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bb885-200">MOF</span><span class="sxs-lookup"><span data-stu-id="bb885-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb885-201"><dt>Cimwin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb885-201"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb885-202">DLL</span><span class="sxs-lookup"><span data-stu-id="bb885-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb885-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb885-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb885-204">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb885-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb885-205">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="bb885-205">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="bb885-206">**Win32 \_ PnPDeviceProperty**</span><span class="sxs-lookup"><span data-stu-id="bb885-206">**Win32\_PnPDeviceProperty**</span></span>](win32-pnpdeviceproperty.md)
</dt> <dt>

[<span data-ttu-id="bb885-207">**GetDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="bb885-207">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md)
</dt> </dl>

 

 




