---
title: 'GUESTOSVERSIONINFOEX 結構 (VPCCOMInterfaces .h) '
description: 包含客體作業系統的作業系統版本資訊。
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- GUESTOSVERSIONINFOEX 結構虛擬電腦
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104279"
---
# <a name="guestosversioninfoex-structure"></a><span data-ttu-id="39fe6-104">GUESTOSVERSIONINFOEX 結構</span><span class="sxs-lookup"><span data-stu-id="39fe6-104">GUESTOSVERSIONINFOEX structure</span></span>

<span data-ttu-id="39fe6-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="39fe6-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="39fe6-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="39fe6-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="39fe6-107">包含客體作業系統的作業系統版本資訊。</span><span class="sxs-lookup"><span data-stu-id="39fe6-107">Contains operating system version information for the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="39fe6-108">語法</span><span class="sxs-lookup"><span data-stu-id="39fe6-108">Syntax</span></span>


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a><span data-ttu-id="39fe6-109">成員</span><span class="sxs-lookup"><span data-stu-id="39fe6-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="39fe6-110">**dwOSVersionInfoSize**</span><span class="sxs-lookup"><span data-stu-id="39fe6-110">**dwOSVersionInfoSize**</span></span>
</dt> <dd>

<span data-ttu-id="39fe6-111">此資料結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="39fe6-111">The size of this data structure, in bytes.</span></span> <span data-ttu-id="39fe6-112">將這個成員設定為 `sizeof(GUESTOSVERSIONINFOEX)` 。</span><span class="sxs-lookup"><span data-stu-id="39fe6-112">Set this member to `sizeof(GUESTOSVERSIONINFOEX)`.</span></span>

</dd> <dt>

<span data-ttu-id="39fe6-113">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="39fe6-113">**dwMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="39fe6-114">主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="39fe6-114">The major version number.</span></span>

</dd> <dt>

<span data-ttu-id="39fe6-115">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="39fe6-115">**dwMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="39fe6-116">次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="39fe6-116">The minor version number.</span></span>

</dd> <dt>

<span data-ttu-id="39fe6-117">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="39fe6-117">**dwBuildNumber**</span></span>
</dt> <dd>

<span data-ttu-id="39fe6-118">組建編號。</span><span class="sxs-lookup"><span data-stu-id="39fe6-118">The build number.</span></span>

</dd> <dt>

<span data-ttu-id="39fe6-119">**dwPlatformId**</span><span class="sxs-lookup"><span data-stu-id="39fe6-119">**dwPlatformId**</span></span>
</dt> <dd>

<span data-ttu-id="39fe6-120">作業系統平臺。</span><span class="sxs-lookup"><span data-stu-id="39fe6-120">The operating system platform.</span></span> <span data-ttu-id="39fe6-121">此成員可以是 **\_ PLATFORM \_ WIN32 \_ NT** (2) 。</span><span class="sxs-lookup"><span data-stu-id="39fe6-121">This member can be **VER\_PLATFORM\_WIN32\_NT** (2).</span></span>

</dd> <dt>

<span data-ttu-id="39fe6-122">**szCSDVersion**</span><span class="sxs-lookup"><span data-stu-id="39fe6-122">**szCSDVersion**</span></span>
</dt> <dd>

<span data-ttu-id="39fe6-123">以 null 終止的字串，例如 "Service Pack 3"，表示系統上安裝的最新 Service Pack。</span><span class="sxs-lookup"><span data-stu-id="39fe6-123">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="39fe6-124">如果未安裝 Service Pack，則字串是空的。</span><span class="sxs-lookup"><span data-stu-id="39fe6-124">If no Service Pack has been installed, the string is empty.</span></span>

</dd> <dt>

<span data-ttu-id="39fe6-125">**wServicePackMajor**</span><span class="sxs-lookup"><span data-stu-id="39fe6-125">**wServicePackMajor**</span></span>
</dt> <dd>

<span data-ttu-id="39fe6-126">已安裝最新 Service Pack 的主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="39fe6-126">The major version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="39fe6-127">**wServicePackMinor**</span><span class="sxs-lookup"><span data-stu-id="39fe6-127">**wServicePackMinor**</span></span>
</dt> <dd>

<span data-ttu-id="39fe6-128">已安裝最新 Service Pack 的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="39fe6-128">The minor version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="39fe6-129">**wSuiteMask**</span><span class="sxs-lookup"><span data-stu-id="39fe6-129">**wSuiteMask**</span></span>
</dt> <dd>

<span data-ttu-id="39fe6-130">識別系統上可用之產品套件的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="39fe6-130">A bitmask that identifies the product suites available on the system.</span></span> <span data-ttu-id="39fe6-131">這個成員可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="39fe6-131">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="39fe6-132">值</span><span class="sxs-lookup"><span data-stu-id="39fe6-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="39fe6-133">意義</span><span class="sxs-lookup"><span data-stu-id="39fe6-133">Meaning</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <span data-ttu-id="39fe6-134"><dt>**VER \_SUITE \_ BACKOFFICE**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-134"><dt>**VER\_SUITE\_BACKOFFICE**</dt> <dt>0x00000004</dt></span></span> </dl>                                            | <span data-ttu-id="39fe6-135">已安裝 Microsoft BackOffice 元件。</span><span class="sxs-lookup"><span data-stu-id="39fe6-135">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <span data-ttu-id="39fe6-136"><dt>**VER \_SUITE \_ BLADE**</dt> <dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-136"><dt>**VER\_SUITE\_BLADE**</dt> <dt>0x00000400</dt></span></span> </dl>                                                           | <span data-ttu-id="39fe6-137">已安裝 Windows Server 2003 （Web Edition）。</span><span class="sxs-lookup"><span data-stu-id="39fe6-137">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <span data-ttu-id="39fe6-138"><dt>**VER \_SUITE \_ COMPUTE \_ SERVER**</dt> <dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-138"><dt>**VER\_SUITE\_COMPUTE\_SERVER**</dt> <dt>0x00004000</dt></span></span> </dl>                               | <span data-ttu-id="39fe6-139">已安裝 Windows Server 2003、Compute Cluster Edition。</span><span class="sxs-lookup"><span data-stu-id="39fe6-139">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <span data-ttu-id="39fe6-140"><dt>**VER \_SUITE \_ DATACENTER**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-140"><dt>**VER\_SUITE\_DATACENTER**</dt> <dt>0x00000080</dt></span></span> </dl>                                            | <span data-ttu-id="39fe6-141">已安裝 windows Server 2008 Datacenter、Windows Server 2003、Datacenter Edition 或 Windows 2000 Datacenter Server。</span><span class="sxs-lookup"><span data-stu-id="39fe6-141">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <span data-ttu-id="39fe6-142"><dt>**VER \_SUITE \_ 企業**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-142"><dt>**VER\_SUITE\_ENTERPRISE**</dt> <dt>0x00000002</dt></span></span> </dl>                                            | <span data-ttu-id="39fe6-143">已安裝 windows Server 2008 Enterprise、Windows Server 2003、Enterprise Edition 或 Windows 2000 Advanced Server。</span><span class="sxs-lookup"><span data-stu-id="39fe6-143">Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="39fe6-144">如需此位旗標的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="39fe6-144">Refer to the Remarks section for more information about this bit flag.</span></span><br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <span data-ttu-id="39fe6-145"><dt>**VER \_SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-145"><dt>**VER\_SUITE\_EMBEDDEDNT**</dt> <dt>0x00000040</dt></span></span> </dl>                                            | <span data-ttu-id="39fe6-146">已安裝 Windows XP Embedded。</span><span class="sxs-lookup"><span data-stu-id="39fe6-146">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <span data-ttu-id="39fe6-147"><dt>**VER \_SUITE \_ 個人**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-147"><dt>**VER\_SUITE\_PERSONAL**</dt> <dt>0x00000200</dt></span></span> </dl>                                                  | <span data-ttu-id="39fe6-148">已安裝 windows Vista Home Premium、Windows Vista Home Basic 或 Windows XP Home Edition。</span><span class="sxs-lookup"><span data-stu-id="39fe6-148">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <span data-ttu-id="39fe6-149"><dt>**VER \_SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-149"><dt>**VER\_SUITE\_SINGLEUSERTS**</dt> <dt>0x00000100</dt></span></span> </dl>                                      | <span data-ttu-id="39fe6-150">支援遠端桌面，但只支援一個互動式會話。</span><span class="sxs-lookup"><span data-stu-id="39fe6-150">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="39fe6-151">除非系統是在應用程式伺服器模式中執行，否則會設定此值。</span><span class="sxs-lookup"><span data-stu-id="39fe6-151">This value is set unless the system is running in application server mode.</span></span><br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <span data-ttu-id="39fe6-152"><dt>**VER \_SUITE \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-152"><dt>**VER\_SUITE\_SMALLBUSINESS**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="39fe6-153">Microsoft Small Business Server 已安裝在系統上，但可能已升級至另一個版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="39fe6-153">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="39fe6-154">如需此位旗標的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="39fe6-154">Refer to the Remarks section for more information about this bit flag.</span></span><br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <span data-ttu-id="39fe6-155"><dt>**VER \_SUITE \_ SMALLBUSINESS \_ 受限**</dt>的 <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-155"><dt>**VER\_SUITE\_SMALLBUSINESS\_RESTRICTED**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="39fe6-156">Microsoft Small Business Server 會以強制的嚴格用戶端授權安裝。</span><span class="sxs-lookup"><span data-stu-id="39fe6-156">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="39fe6-157">如需此位旗標的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="39fe6-157">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <span data-ttu-id="39fe6-158"><dt>**VER \_SUITE \_ STORAGE \_ SERVER**</dt> <dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-158"><dt>**VER\_SUITE\_STORAGE\_SERVER**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="39fe6-159">已安裝 windows Storage Server 2003 R2 或 Windows Storage Server 2003is。</span><span class="sxs-lookup"><span data-stu-id="39fe6-159">Windows Storage Server 2003 R2 or Windows Storage Server 2003is installed.</span></span><br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <span data-ttu-id="39fe6-160"><dt>**VER \_SUITE \_ 終端**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-160"><dt>**VER\_SUITE\_TERMINAL**</dt> <dt>0x00000010</dt></span></span> </dl>                                                  | <span data-ttu-id="39fe6-161">已安裝終端機服務。</span><span class="sxs-lookup"><span data-stu-id="39fe6-161">Terminal Services is installed.</span></span> <span data-ttu-id="39fe6-162">一律會設定這個值。</span><span class="sxs-lookup"><span data-stu-id="39fe6-162">This value is always set.</span></span><br/> <span data-ttu-id="39fe6-163">如果設定了 **ver \_ suite \_ 終端** 機，但未設定 **ver \_ suite \_ SINGLEUSERTS** ，系統就會在應用程式伺服器模式中執行。</span><span class="sxs-lookup"><span data-stu-id="39fe6-163">If **VER\_SUITE\_TERMINAL** is set but **VER\_SUITE\_SINGLEUSERTS** is not set, the system is running in application server mode.</span></span><br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <span data-ttu-id="39fe6-164"><dt>**VER \_SUITE \_ WH \_ 伺服器**</dt> <dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-164"><dt>**VER\_SUITE\_WH\_SERVER**</dt> <dt>0x00008000</dt></span></span> </dl>                                              | <span data-ttu-id="39fe6-165">已安裝 Windows Home Server。</span><span class="sxs-lookup"><span data-stu-id="39fe6-165">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="39fe6-166">**wProductType**</span><span class="sxs-lookup"><span data-stu-id="39fe6-166">**wProductType**</span></span>
</dt> <dd>

<span data-ttu-id="39fe6-167">系統的任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="39fe6-167">Any additional information about the system.</span></span> <span data-ttu-id="39fe6-168">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="39fe6-168">This member can be one of the following values.</span></span>



| <span data-ttu-id="39fe6-169">值</span><span class="sxs-lookup"><span data-stu-id="39fe6-169">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="39fe6-170">意義</span><span class="sxs-lookup"><span data-stu-id="39fe6-170">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <span data-ttu-id="39fe6-171"><dt>**VER \_NT \_ 域 \_ 控制器**</dt> <dt>0x0000002</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-171"><dt>**VER\_NT\_DOMAIN\_CONTROLLER**</dt> <dt>0x0000002</dt></span></span> </dl> | <span data-ttu-id="39fe6-172">系統是網域控制站，而作業系統是 Windows Server 2008 R2、Windows Server 2008、Windows Server 2003 R2、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="39fe6-172">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <span data-ttu-id="39fe6-173"><dt>**VER \_NT \_ 伺服器**</dt> <dt>0x0000003</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-173"><dt>**VER\_NT\_SERVER**</dt> <dt>0x0000003</dt></span></span> </dl>                                   | <span data-ttu-id="39fe6-174">作業系統是 Windows Server 2008 R2、Windows Server 2008、Windows Server 2003 R2、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="39fe6-174">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="39fe6-175">請注意，同時也是網域控制站的伺服器會回報為 **ver \_ nt \_ 域 \_ 控制器**，而不是 **\_ nt \_ server**。</span><span class="sxs-lookup"><span data-stu-id="39fe6-175">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <span data-ttu-id="39fe6-176"><dt>**VER \_NT \_ 工作站**</dt> <dt>0x0000001</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-176"><dt>**VER\_NT\_WORKSTATION**</dt> <dt>0x0000001</dt></span></span> </dl>                    | <span data-ttu-id="39fe6-177">作業系統是 Windows 7、Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="39fe6-177">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="39fe6-178">**wReserved**</span><span class="sxs-lookup"><span data-stu-id="39fe6-178">**wReserved**</span></span>
</dt> <dd>

<span data-ttu-id="39fe6-179">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="39fe6-179">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39fe6-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="39fe6-180">Requirements</span></span>



| <span data-ttu-id="39fe6-181">需求</span><span class="sxs-lookup"><span data-stu-id="39fe6-181">Requirement</span></span> | <span data-ttu-id="39fe6-182">值</span><span class="sxs-lookup"><span data-stu-id="39fe6-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39fe6-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39fe6-183">Minimum supported client</span></span><br/> | <span data-ttu-id="39fe6-184">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39fe6-184">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39fe6-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39fe6-185">Minimum supported server</span></span><br/> | <span data-ttu-id="39fe6-186">都不支援</span><span class="sxs-lookup"><span data-stu-id="39fe6-186">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="39fe6-187">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="39fe6-187">End of client support</span></span><br/>    | <span data-ttu-id="39fe6-188">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39fe6-188">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39fe6-189">產品</span><span class="sxs-lookup"><span data-stu-id="39fe6-189">Product</span></span><br/>                  | <span data-ttu-id="39fe6-190">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="39fe6-190">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="39fe6-191">標頭</span><span class="sxs-lookup"><span data-stu-id="39fe6-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="39fe6-192"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-192"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39fe6-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39fe6-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39fe6-194">**IVMGuestOS::GetOsVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="39fe6-194">**IVMGuestOS::GetOsVersionInfo**</span></span>](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

