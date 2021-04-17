---
description: 代表 Win32 \_ PnPEntity：： GetDeviceProperties 方法所傳回之屬性的類別基底類型。
ms.assetid: f636c106-6ca6-407f-804a-0ec554ed565c
ms.tgt_platform: multiple
title: Win32_PnPDeviceProperty 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDeviceProperty
- Win32_PnPDeviceProperty.Key
- Win32_PnPDeviceProperty.KeyName
- Win32_PnPDeviceProperty.Type
- Win32_PnPDeviceProperty.DeviceID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8e1869e5d6cde35404ff9c12eabd35631b3227c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468561"
---
# <a name="win32_pnpdeviceproperty-class"></a><span data-ttu-id="6c0d3-103">Win32 \_ PnPDeviceProperty 類別</span><span class="sxs-lookup"><span data-stu-id="6c0d3-103">Win32\_PnPDeviceProperty class</span></span>

<span data-ttu-id="6c0d3-104">代表 [**Win32 \_ PnPEntity**](win32-pnpentity.md)：：[**GetDeviceProperties**](getdeviceproperties-win32-pnpentity.md) 方法所傳回之屬性的類別基底類型。</span><span class="sxs-lookup"><span data-stu-id="6c0d3-104">The base type for classes representing a property returned by the [**Win32\_PnPEntity**](win32-pnpentity.md)::[**GetDeviceProperties**](getdeviceproperties-win32-pnpentity.md) Method.</span></span>

<span data-ttu-id="6c0d3-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6c0d3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c0d3-106">語法</span><span class="sxs-lookup"><span data-stu-id="6c0d3-106">Syntax</span></span>

``` syntax
[abstract, UUID("{ee0b76cd-314b-41f1-99d4-d4f3b0421430}"), AMENDMENT]
class Win32_PnPDeviceProperty
{
  string Key;
  string KeyName;
  Uint32 Type;
  string DeviceID;
};
```

## <a name="members"></a><span data-ttu-id="6c0d3-107">成員</span><span class="sxs-lookup"><span data-stu-id="6c0d3-107">Members</span></span>

<span data-ttu-id="6c0d3-108">**Win32 \_ PnPDeviceProperty** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6c0d3-108">The **Win32\_PnPDeviceProperty** class has these types of members:</span></span>

-   [<span data-ttu-id="6c0d3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6c0d3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c0d3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6c0d3-110">Properties</span></span>

<span data-ttu-id="6c0d3-111">**Win32 \_ PnPDeviceProperty** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6c0d3-111">The **Win32\_PnPDeviceProperty** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c0d3-112">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-112">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c0d3-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c0d3-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c0d3-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c0d3-115">識別 PnP 裝置。</span><span class="sxs-lookup"><span data-stu-id="6c0d3-115">Identifies the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="6c0d3-116">**金鑰**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-116">**Key**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c0d3-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c0d3-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c0d3-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c0d3-119">識別 **資料** 屬性之索引鍵 Name-Value 組的值。</span><span class="sxs-lookup"><span data-stu-id="6c0d3-119">The value of the Key Name-Value pair that identifies the **Data** property.</span></span>

</dd> <dt>

<span data-ttu-id="6c0d3-120">**KeyName**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-120">**KeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c0d3-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c0d3-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c0d3-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c0d3-123">識別 **資料** 屬性之索引鍵 Name-Value 組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c0d3-123">The name of the Key Name-Value pair that identifies the **Data** property.</span></span>

</dd> <dt>

<span data-ttu-id="6c0d3-124">**型別**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-124">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c0d3-125">資料類型： **Uint32**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-125">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c0d3-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c0d3-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c0d3-127">**資料** 屬性的型別。</span><span class="sxs-lookup"><span data-stu-id="6c0d3-127">The type of the **Data** property.</span></span>

<span data-ttu-id="6c0d3-128">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="6c0d3-128">The possible values are.</span></span>

<dt>

<span id="Empty"></span><span id="empty"></span><span id="EMPTY"></span>

<span data-ttu-id="6c0d3-129">**空白** (0) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-129">**Empty** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Null"></span><span id="null"></span><span id="NULL"></span>

<span data-ttu-id="6c0d3-130">**Null** (1) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-130">**Null** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SByte"></span><span id="sbyte"></span><span id="SBYTE"></span>

<span data-ttu-id="6c0d3-131">**SByte** (2) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-131">**SByte** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Byte"></span><span id="byte"></span><span id="BYTE"></span>

<span data-ttu-id="6c0d3-132">**Byte** (3) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-132">**Byte** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16"></span><span id="int16"></span><span id="INT16"></span>

<span data-ttu-id="6c0d3-133">**Int16** (4) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-133">**Int16** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16"></span><span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="6c0d3-134">**UInt16** (5) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-134">**UInt16** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Int32"></span><span id="int32"></span><span id="INT32"></span>

<span data-ttu-id="6c0d3-135">**Int32** (6) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-135">**Int32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Uint32"></span><span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="6c0d3-136">**Uint32** (7) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-136">**Uint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64"></span><span id="int64"></span><span id="INT64"></span>

<span data-ttu-id="6c0d3-137">**Int64** (8) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-137">**Int64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64"></span><span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="6c0d3-138">**UInt64** (9) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-138">**UInt64** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Float"></span><span id="float"></span><span id="FLOAT"></span>

<span data-ttu-id="6c0d3-139">**Float** (10) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-139">**Float** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Double"></span><span id="double"></span><span id="DOUBLE"></span>

<span data-ttu-id="6c0d3-140">**Double** (11) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-140">**Double** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Decimal"></span><span id="decimal"></span><span id="DECIMAL"></span>

<span data-ttu-id="6c0d3-141">**Decimal** (12) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-141">**Decimal** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Guid"></span><span id="guid"></span><span id="GUID"></span>

<span data-ttu-id="6c0d3-142">**Guid** (13) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-142">**Guid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Currency"></span><span id="currency"></span><span id="CURRENCY"></span>

<span data-ttu-id="6c0d3-143">**Currency** (14) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-143">**Currency** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Date"></span><span id="date"></span><span id="DATE"></span>

<span data-ttu-id="6c0d3-144">**日期** (15) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-144">**Date** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTime"></span><span id="filetime"></span><span id="FILETIME"></span>

<span data-ttu-id="6c0d3-145">**FileTime** (16) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-145">**FileTime** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="6c0d3-146">**布林值** (17) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-146">**Boolean** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="String"></span><span id="string"></span><span id="STRING"></span>

<span data-ttu-id="6c0d3-147">**字串** (18) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-147">**String** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptor"></span><span id="securitydescriptor"></span><span id="SECURITYDESCRIPTOR"></span>

<span data-ttu-id="6c0d3-148">**SecurityDescriptor** (19) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-148">**SecurityDescriptor** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorString"></span><span id="securitydescriptorstring"></span><span id="SECURITYDESCRIPTORSTRING"></span>

<span data-ttu-id="6c0d3-149">**SecurityDescriptorString** (20) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-149">**SecurityDescriptorString** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEY"></span><span id="devpropkey"></span>

<span data-ttu-id="6c0d3-150">**DEVPROPKEY** (21) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-150">**DEVPROPKEY** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPE"></span><span id="devproptype"></span>

<span data-ttu-id="6c0d3-151">**DEVPROPTYPE** (22) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-151">**DEVPROPTYPE** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6c0d3-152">**錯誤** (23) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-152">**Error** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatus"></span><span id="ntstatus"></span><span id="NTSTATUS"></span>

<span data-ttu-id="6c0d3-153"> (24) 的 **NTStatus**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-153">**NTStatus** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirect"></span><span id="stringindirect"></span><span id="STRINGINDIRECT"></span>

<span data-ttu-id="6c0d3-154">**StringIndirect** (25) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-154">**StringIndirect** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="6c0d3-155">**已保留**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-155">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="6c0d3-156">26–4097</span><span class="sxs-lookup"><span data-stu-id="6c0d3-156">26–4097</span></span></dd> <dt>

<span id="SByteArray"></span><span id="sbytearray"></span><span id="SBYTEARRAY"></span>

<span data-ttu-id="6c0d3-157">**SByteArray** (4098) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-157">**SByteArray** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="6c0d3-158">**Binary** (4099) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-158">**Binary** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16Array"></span><span id="int16array"></span><span id="INT16ARRAY"></span>

<span data-ttu-id="6c0d3-159">**Int16Array** (4100) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-159">**Int16Array** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16Array"></span><span id="uint16array"></span><span id="UINT16ARRAY"></span>

<span data-ttu-id="6c0d3-160">**UInt16Array** (4101) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-160">**UInt16Array** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64Array"></span><span id="int64array"></span><span id="INT64ARRAY"></span>

<span data-ttu-id="6c0d3-161">**Int64Array** (4102) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-161">**Int64Array** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64Array"></span><span id="uint64array"></span><span id="UINT64ARRAY"></span>

<span data-ttu-id="6c0d3-162">**UInt64Array** (4103) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-162">**UInt64Array** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="FloatArray"></span><span id="floatarray"></span><span id="FLOATARRAY"></span>

<span data-ttu-id="6c0d3-163">**FloatArray** (4104) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-163">**FloatArray** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="DoubleArray"></span><span id="doublearray"></span><span id="DOUBLEARRAY"></span>

<span data-ttu-id="6c0d3-164">**DoubleArray** (4105) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-164">**DoubleArray** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="DecimalArray"></span><span id="decimalarray"></span><span id="DECIMALARRAY"></span>

<span data-ttu-id="6c0d3-165">**DecimalArray** (4106) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-165">**DecimalArray** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="GuidArray"></span><span id="guidarray"></span><span id="GUIDARRAY"></span>

<span data-ttu-id="6c0d3-166">**GuidArray** (4107) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-166">**GuidArray** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="CurrencyArray"></span><span id="currencyarray"></span><span id="CURRENCYARRAY"></span>

<span data-ttu-id="6c0d3-167">**CurrencyArray** (4108) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-167">**CurrencyArray** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="DateArray"></span><span id="datearray"></span><span id="DATEARRAY"></span>

<span data-ttu-id="6c0d3-168">**DateArray** (4109) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-168">**DateArray** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTimeArray"></span><span id="filetimearray"></span><span id="FILETIMEARRAY"></span>

<span data-ttu-id="6c0d3-169">**FileTimeArray** (4110) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-169">**FileTimeArray** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="BooleanArray"></span><span id="booleanarray"></span><span id="BOOLEANARRAY"></span>

<span data-ttu-id="6c0d3-170">**BooleanArray** (4111) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-170">**BooleanArray** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="StringList"></span><span id="stringlist"></span><span id="STRINGLIST"></span>

<span data-ttu-id="6c0d3-171">**StringList** (4112) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-171">**StringList** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorList"></span><span id="securitydescriptorlist"></span><span id="SECURITYDESCRIPTORLIST"></span>

<span data-ttu-id="6c0d3-172">**SecurityDescriptorList** (4113) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-172">**SecurityDescriptorList** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorStringList"></span><span id="securitydescriptorstringlist"></span><span id="SECURITYDESCRIPTORSTRINGLIST"></span>

<span data-ttu-id="6c0d3-173">**SecurityDescriptorStringList** (8210) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-173">**SecurityDescriptorStringList** (8210)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEYArray"></span><span id="devpropkeyarray"></span><span id="DEVPROPKEYARRAY"></span>

<span data-ttu-id="6c0d3-174">**DEVPROPKEYArray** (8211) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-174">**DEVPROPKEYArray** (8211)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPEArray"></span><span id="devproptypearray"></span><span id="DEVPROPTYPEARRAY"></span>

<span data-ttu-id="6c0d3-175">**DEVPROPTYPEArray** (8212) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-175">**DEVPROPTYPEArray** (8212)</span></span>


</dt> <dd></dd> <dt>

<span id="ErrorArray"></span><span id="errorarray"></span><span id="ERRORARRAY"></span>

<span data-ttu-id="6c0d3-176">**ErrorArray** (4117) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-176">**ErrorArray** (4117)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatusArray"></span><span id="ntstatusarray"></span><span id="NTSTATUSARRAY"></span>

<span data-ttu-id="6c0d3-177">**NTStatusArray** (4118) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-177">**NTStatusArray** (4118)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirectList"></span><span id="stringindirectlist"></span><span id="STRINGINDIRECTLIST"></span>

<span data-ttu-id="6c0d3-178">**StringIndirectList** (4119) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-178">**StringIndirectList** (4119)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_-_check_in_devpropdef.h"></span><span id="unknown_-_check_in_devpropdef.h"></span><span id="UNKNOWN_-_CHECK_IN_DEVPROPDEF.H"></span>

<span data-ttu-id="6c0d3-179">**未知-在 devpropdef 中檢查** (4120) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-179">**Unknown - check in devpropdef.h** (4120)</span></span>


</dt> <dd></dd> <dt>

<span id="TBD"></span><span id="tbd"></span>

<span data-ttu-id="6c0d3-180">**TBD** (8217) </span><span class="sxs-lookup"><span data-stu-id="6c0d3-180">**TBD** (8217)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="6c0d3-181">**已保留**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-181">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="6c0d3-182">8218–4294967295</span><span class="sxs-lookup"><span data-stu-id="6c0d3-182">8218–4294967295</span></span></dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c0d3-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c0d3-183">Requirements</span></span>



| <span data-ttu-id="6c0d3-184">需求</span><span class="sxs-lookup"><span data-stu-id="6c0d3-184">Requirement</span></span> | <span data-ttu-id="6c0d3-185">值</span><span class="sxs-lookup"><span data-stu-id="6c0d3-185">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c0d3-186">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c0d3-186">Minimum supported client</span></span><br/> | <span data-ttu-id="6c0d3-187">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c0d3-187">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6c0d3-188">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c0d3-188">Minimum supported server</span></span><br/> | <span data-ttu-id="6c0d3-189">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6c0d3-189">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="6c0d3-190">命名空間</span><span class="sxs-lookup"><span data-stu-id="6c0d3-190">Namespace</span></span><br/>                | <span data-ttu-id="6c0d3-191">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6c0d3-191">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c0d3-192">MOF</span><span class="sxs-lookup"><span data-stu-id="6c0d3-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c0d3-193"><dt>Cimwin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c0d3-193"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c0d3-194">DLL</span><span class="sxs-lookup"><span data-stu-id="6c0d3-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c0d3-195"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c0d3-195"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c0d3-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c0d3-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c0d3-197">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="6c0d3-197">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="6c0d3-198">**GetDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="6c0d3-198">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md)
</dt> </dl>

 

 
