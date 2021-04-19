---
description: 表示元件物件模型 (COM) 元件的設定。
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Win32_ClassicCOMClassSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970539"
---
# <a name="win32_classiccomclasssetting-class"></a><span data-ttu-id="ee860-103">Win32 \_ ClassicCOMClassSetting 類別</span><span class="sxs-lookup"><span data-stu-id="ee860-103">Win32\_ClassicCOMClassSetting class</span></span>

<span data-ttu-id="ee860-104">**Win32 \_ ClassicCOMClassSetting** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表元件物件模型 (COM) 元件的設定。</span><span class="sxs-lookup"><span data-stu-id="ee860-104">The **Win32\_ClassicCOMClassSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="ee860-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ee860-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ee860-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ee860-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee860-107">語法</span><span class="sxs-lookup"><span data-stu-id="ee860-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a><span data-ttu-id="ee860-108">成員</span><span class="sxs-lookup"><span data-stu-id="ee860-108">Members</span></span>

<span data-ttu-id="ee860-109">**Win32 \_ ClassicCOMClassSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ee860-109">The **Win32\_ClassicCOMClassSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="ee860-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ee860-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee860-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ee860-111">Properties</span></span>

<span data-ttu-id="ee860-112">**Win32 \_ ClassicCOMClassSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ee860-112">The **Win32\_ClassicCOMClassSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee860-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="ee860-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-116">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ AppID \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[AppID\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-117">全域唯一識別碼 (使用此 COM 元件之 COM 應用程式的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="ee860-117">Globally unique identifier (GUID) for the COM application using this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-118">**AutoConvertToClsid**</span><span class="sxs-lookup"><span data-stu-id="ee860-118">**AutoConvertToClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-121">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoConvertTo \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoConvertTo\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-122">將自動轉換此 COM 元件之 COM 類別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ee860-122">GUID of the COM class to which this COM component will automatically be converted.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-123">**AutoTreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="ee860-123">**AutoTreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-126">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoTreatAs \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-126">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoTreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-127">將自動模擬這個類別之實例的 COM 元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ee860-127">GUID for the COM component that will automatically emulate instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-128">**標題**</span><span class="sxs-lookup"><span data-stu-id="ee860-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-131">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="ee860-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ee860-132">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="ee860-132">Short textual description of the current object.</span></span>

<span data-ttu-id="ee860-133">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="ee860-133">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee860-134">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="ee860-134">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-137">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-138">此 COM 元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ee860-138">GUID of this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-139">**控制**</span><span class="sxs-lookup"><span data-stu-id="ee860-139">**Control**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-140">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ee860-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-142">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Control" ) </span><span class="sxs-lookup"><span data-stu-id="ee860-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Control")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-143">COM 元件是一個 OLE 控制項。</span><span class="sxs-lookup"><span data-stu-id="ee860-143">COM component is an OLE control.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-144">**DefaultIcon**</span><span class="sxs-lookup"><span data-stu-id="ee860-144">**DefaultIcon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-147">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\DefaultIcon\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-148">可執行檔的路徑，以及類別使用之預設圖示的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee860-148">Path to the executable file and resource identifier of the default icon used by the class.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-149">**說明**</span><span class="sxs-lookup"><span data-stu-id="ee860-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee860-152">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="ee860-152">Textual description of the current object.</span></span>

<span data-ttu-id="ee860-153">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="ee860-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee860-154">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="ee860-154">**InprocHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-157">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-158">COM 元件之16位自訂處理常式的完整路徑，包括檔案名或僅檔案名。</span><span class="sxs-lookup"><span data-stu-id="ee860-158">Full path including filename or only filename to a 16-bit custom handler for the COM component.</span></span> <span data-ttu-id="ee860-159">提供者不一定會傳回完整的路徑。</span><span class="sxs-lookup"><span data-stu-id="ee860-159">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-160">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="ee860-160">**InprocHandler32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-163">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-164">COM 元件之32位自訂處理常式的完整路徑，包括檔案名或僅檔案名。</span><span class="sxs-lookup"><span data-stu-id="ee860-164">Full path including filename or only filename to a 32-bit custom handler for the COM component.</span></span> <span data-ttu-id="ee860-165">提供者不一定會傳回完整的路徑。</span><span class="sxs-lookup"><span data-stu-id="ee860-165">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-166">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="ee860-166">**InprocServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-169">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-170">此 COM 元件的完整路徑（包含檔案名或僅檔案名）至16位同進程伺服器 DLL。</span><span class="sxs-lookup"><span data-stu-id="ee860-170">Full path including filename or only filename to a 16-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="ee860-171">提供者不一定會傳回完整的路徑。</span><span class="sxs-lookup"><span data-stu-id="ee860-171">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-172">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="ee860-172">**InprocServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-175">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-176">此 COM 元件的完整路徑（包含檔案名）或僅限32位同進程伺服器 DLL 的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ee860-176">Full path including filename or only filename to a 32-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="ee860-177">提供者不一定會傳回完整的路徑。</span><span class="sxs-lookup"><span data-stu-id="ee860-177">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-178">**插入**</span><span class="sxs-lookup"><span data-stu-id="ee860-178">**Insertable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-179">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ee860-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-181">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} 「 \\ \\ 插入」 ) </span><span class="sxs-lookup"><span data-stu-id="ee860-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Insertable")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-182">COM 元件可以插入至 OLE 容器應用程式。</span><span class="sxs-lookup"><span data-stu-id="ee860-182">COM component can be inserted into OLE container applications.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-183">**JAVAClass**</span><span class="sxs-lookup"><span data-stu-id="ee860-183">**JavaClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-184">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ee860-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-186">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ JAVAClass \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[JavaClass\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-187">COM 元件是 JAVA 元件。</span><span class="sxs-lookup"><span data-stu-id="ee860-187">COM component is a Java component.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-188">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="ee860-188">**LocalServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-191">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-192">完整路徑（包括檔案名），或只包含檔案名至16位本機伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="ee860-192">Full path including filename or only filename to a 16-bit local server application.</span></span> <span data-ttu-id="ee860-193">提供者不一定會傳回完整的路徑。</span><span class="sxs-lookup"><span data-stu-id="ee860-193">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-194">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="ee860-194">**LocalServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-197">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-198">包含檔案名的完整路徑，或僅限32位本機伺服器應用程式的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ee860-198">Full path including filename or only filename to a 32-bit local server application.</span></span> <span data-ttu-id="ee860-199">提供者不一定會傳回完整的路徑。</span><span class="sxs-lookup"><span data-stu-id="ee860-199">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-200">**LongDisplayName**</span><span class="sxs-lookup"><span data-stu-id="ee860-200">**LongDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-203">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\3\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-204">COM 應用程式的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="ee860-204">Full name of the COM application.</span></span> <span data-ttu-id="ee860-205">它會用於 [ **OLE 貼上特殊**] 對話方塊的 [**結果**] 欄位等區域中。</span><span class="sxs-lookup"><span data-stu-id="ee860-205">It is used in areas such as the **Results** field of the **OLE Paste Special** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-206">**ProgId**</span><span class="sxs-lookup"><span data-stu-id="ee860-206">**ProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-209">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-209">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ProgID\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-210">與 COM 元件相關聯的程式設計識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee860-210">Programmatic identifier associated with the COM component.</span></span> <span data-ttu-id="ee860-211">ProgID 的格式是 <廠商. <元件。 <版本。</span><span class="sxs-lookup"><span data-stu-id="ee860-211">The format of a ProgID is <Vendor.<Component.<Version.</span></span> <span data-ttu-id="ee860-212">此識別碼不保證是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ee860-212">This identifier is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-213">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="ee860-213">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-216">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="ee860-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ee860-217">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee860-217">Identifier by which the current object is known.</span></span>

<span data-ttu-id="ee860-218">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="ee860-218">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee860-219">**ShortDisplayName**</span><span class="sxs-lookup"><span data-stu-id="ee860-219">**ShortDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-220">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-222">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\2\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-223"> (在功能表和快顯) 中使用的 COM 應用程式的簡短名稱。</span><span class="sxs-lookup"><span data-stu-id="ee860-223">Short name of the COM application (used in menus and pop-ups).</span></span>

</dd> <dt>

<span data-ttu-id="ee860-224">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="ee860-224">**ThreadingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-227">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ >threadingmodel \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[ThreadingModel\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-228">同進程 COM 類別所使用的執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="ee860-228">Threading model used by in-process COM classes.</span></span> <span data-ttu-id="ee860-229">如果此屬性為 **Null**，則不會使用任何執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="ee860-229">If this property is **NULL**, then no threading model is used.</span></span> <span data-ttu-id="ee860-230">元件是在用戶端的主執行緒上建立，而來自其他執行緒的呼叫會封送處理至此執行緒。</span><span class="sxs-lookup"><span data-stu-id="ee860-230">The component is created on the main thread of the client and calls from other threads are marshaled to this thread.</span></span>

<span data-ttu-id="ee860-231">單元模型指定元件只能由一個執行緒輸入。</span><span class="sxs-lookup"><span data-stu-id="ee860-231">The Apartment model specifies that components may be entered by one and only one thread.</span></span> <span data-ttu-id="ee860-232">這些類型的物件服務器所保留的一般資料必須受到保護，以免執行緒衝突，因為物件服務器支援多個元件。</span><span class="sxs-lookup"><span data-stu-id="ee860-232">Common data held by these types of object servers must be protected against thread collisions because the object server supports multiple components.</span></span> <span data-ttu-id="ee860-233">不同的執行緒可以同時輸入每個元件。</span><span class="sxs-lookup"><span data-stu-id="ee860-233">Each component can be entered simultaneously by different threads.</span></span>

<span data-ttu-id="ee860-234">免費模型指定元件對哪些執行緒或可輸入物件的執行緒沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="ee860-234">The Free model specifies that components place no restrictions on which threads or how many threads can enter the object.</span></span> <span data-ttu-id="ee860-235">物件不能包含執行緒特定的資料，而且必須保護其資料，使其無法同時存取多個執行緒。</span><span class="sxs-lookup"><span data-stu-id="ee860-235">The object cannot contain thread-specific data and must protect its data from simultaneous access by multiple threads.</span></span> <span data-ttu-id="ee860-236">但是，無限制執行緒元件無法直接由單元執行緒存取，而且它們的呼叫會從用戶端單元封送處理。</span><span class="sxs-lookup"><span data-stu-id="ee860-236">Free-threaded components however, cannot be accessed by apartment threads directly, and calls to them are marshaled across from the client apartment.</span></span>

<span data-ttu-id="ee860-237">當兩者都指定時，元件可用於單元執行緒或無線程模式。</span><span class="sxs-lookup"><span data-stu-id="ee860-237">When Both is specified, components can be used in either apartment-threaded or free-threaded modes.</span></span> <span data-ttu-id="ee860-238">這些元件可以由多個執行緒輸入、保護其資料免于執行緒衝突，且不包含執行緒特定資料。</span><span class="sxs-lookup"><span data-stu-id="ee860-238">These components can be entered by multiple threads, protect their data from thread collisions, and do not contain thread-specific data.</span></span>

<span data-ttu-id="ee860-239">值如下：</span><span class="sxs-lookup"><span data-stu-id="ee860-239">The values are:</span></span>

<dl> <dd><span data-ttu-id="ee860-240">Apartment</span><span class="sxs-lookup"><span data-stu-id="ee860-240">"Apartment"</span></span></dd> <dd><span data-ttu-id="ee860-241">存在</span><span class="sxs-lookup"><span data-stu-id="ee860-241">"Free"</span></span></dd> <dd><span data-ttu-id="ee860-242">對</span><span class="sxs-lookup"><span data-stu-id="ee860-242">"Both"</span></span></dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

<span data-ttu-id="ee860-243">**公寓** ( 「單元」 ) </span><span class="sxs-lookup"><span data-stu-id="ee860-243">**Apartment** ("Apartment")</span></span>


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

<span data-ttu-id="ee860-244">**免費** ( 「免費」 ) </span><span class="sxs-lookup"><span data-stu-id="ee860-244">**Free** ("Free")</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="ee860-245">**兩者都** ( 「兩者」 ) </span><span class="sxs-lookup"><span data-stu-id="ee860-245">**Both** ("Both")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ee860-246">**ToolBoxBitmap32**</span><span class="sxs-lookup"><span data-stu-id="ee860-246">**ToolBoxBitmap32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-249">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ToolBoxBitmap32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-250">適用于 [工具列] 或 [工具箱] 按鈕臉部的小型 (16x16) 點陣圖的模組名稱和資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee860-250">Module name and resource identifier for a small (16x16) bitmap used for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="ee860-251">當 COM 元件是 OLE 或 ActiveX 控制項時使用。</span><span class="sxs-lookup"><span data-stu-id="ee860-251">Used when the COM component is an OLE or ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-252">**TreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="ee860-252">**TreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-253">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-255">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ TreatAs \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-255">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-256">可以模擬此元件之實例的 COM 元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ee860-256">GUID of a COM component that can emulate instances of this component.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-257">**TypeLibraryId**</span><span class="sxs-lookup"><span data-stu-id="ee860-257">**TypeLibraryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-260">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ TypeLib \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-260">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TypeLib\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-261">此 COM 元件之類型程式庫的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ee860-261">GUID for the type library for this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-262">**版本**</span><span class="sxs-lookup"><span data-stu-id="ee860-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-263">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-265">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Version \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Version\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-266">這個 COM 類別的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="ee860-266">Version number of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="ee860-267">**VersionIndependentProgId**</span><span class="sxs-lookup"><span data-stu-id="ee860-267">**VersionIndependentProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee860-268">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee860-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee860-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee860-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee860-270">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgId \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="ee860-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\VersionIndependentProgId\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="ee860-271">相同程式的所有版本都是一致的程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee860-271">Program identifier that is consistent for all versions of the same program.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee860-272">備註</span><span class="sxs-lookup"><span data-stu-id="ee860-272">Remarks</span></span>

<span data-ttu-id="ee860-273">**Win32 \_ ClassicCOMClassSetting** 類別衍生自 [**win32 \_ COMSetting**](win32-comsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="ee860-273">The **Win32\_ClassicCOMClassSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee860-274">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee860-274">Requirements</span></span>



| <span data-ttu-id="ee860-275">需求</span><span class="sxs-lookup"><span data-stu-id="ee860-275">Requirement</span></span> | <span data-ttu-id="ee860-276">值</span><span class="sxs-lookup"><span data-stu-id="ee860-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee860-277">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee860-277">Minimum supported client</span></span><br/> | <span data-ttu-id="ee860-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee860-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee860-279">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee860-279">Minimum supported server</span></span><br/> | <span data-ttu-id="ee860-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee860-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee860-281">命名空間</span><span class="sxs-lookup"><span data-stu-id="ee860-281">Namespace</span></span><br/>                | <span data-ttu-id="ee860-282">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ee860-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ee860-283">MOF</span><span class="sxs-lookup"><span data-stu-id="ee860-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee860-284"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee860-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee860-285">DLL</span><span class="sxs-lookup"><span data-stu-id="ee860-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee860-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee860-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee860-287">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee860-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee860-288">**Win32 \_ COMSetting**</span><span class="sxs-lookup"><span data-stu-id="ee860-288">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="ee860-289">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee860-289">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

