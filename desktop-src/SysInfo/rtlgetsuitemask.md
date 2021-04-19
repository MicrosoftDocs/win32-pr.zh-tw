---
description: 抓取識別系統上可用之產品套件的位元遮罩。 如果在伺服器接收器內容中執行的應用程式中呼叫此函式，則會改為抓取伺服器定址接收器的套件遮罩。
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: 'RtlGetSuiteMask 函式 (Ntddk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997846"
---
# <a name="rtlgetsuitemask-function"></a><span data-ttu-id="58527-104">RtlGetSuiteMask 函式</span><span class="sxs-lookup"><span data-stu-id="58527-104">RtlGetSuiteMask function</span></span>

<span data-ttu-id="58527-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="58527-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="58527-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="58527-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="58527-107">抓取識別系統上可用之產品套件的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="58527-107">Retrieves a bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="58527-108">如果在伺服器接收器內容中執行的應用程式中呼叫此函式，則會改為抓取伺服器定址接收器的套件遮罩。</span><span class="sxs-lookup"><span data-stu-id="58527-108">If this function is called in an application that runs in the context of a server silo, the suite mask for the server silo is retrieved instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="58527-109">語法</span><span class="sxs-lookup"><span data-stu-id="58527-109">Syntax</span></span>


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a><span data-ttu-id="58527-110">參數</span><span class="sxs-lookup"><span data-stu-id="58527-110">Parameters</span></span>

<span data-ttu-id="58527-111">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="58527-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58527-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="58527-112">Return value</span></span>

<span data-ttu-id="58527-113">識別系統上可用之產品套件的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="58527-113">A bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="58527-114">位元遮罩可以包含下列值。</span><span class="sxs-lookup"><span data-stu-id="58527-114">The bit mask can include the following values.</span></span>



| <span data-ttu-id="58527-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="58527-115">Return value</span></span>                                                                          | <span data-ttu-id="58527-116">描述</span><span class="sxs-lookup"><span data-stu-id="58527-116">Description</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58527-117"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="58527-117"><dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="58527-118">Microsoft Small Business Server 已安裝在系統上，但可能已升級至另一個版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="58527-118">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="58527-119">如需此位旗標的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="58527-119">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                           |
| <dl> <span data-ttu-id="58527-120"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="58527-120"><dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="58527-121">已安裝 Windows 10 企業版、Windows 8.1 企業版、Windows Server 2008 Enterprise、Windows Server 2003、Enterprise Edition 或 Windows 2000 Advanced Server。</span><span class="sxs-lookup"><span data-stu-id="58527-121">Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="58527-122">如需此位旗標的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="58527-122">Refer to the Remarks section for more information about this bit flag.</span></span><br/> |
| <dl> <span data-ttu-id="58527-123"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="58527-123"><dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="58527-124">已安裝 Microsoft BackOffice 元件。</span><span class="sxs-lookup"><span data-stu-id="58527-124">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="58527-125"><dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="58527-125"><dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="58527-126">已安裝通訊伺服器2003、communication Server 2005、communication Server 2007 或 communication Server 2007 R2。</span><span class="sxs-lookup"><span data-stu-id="58527-126">Communications Server 2003, Communications Server 2005, Communications Server 2007, or Communications Server 2007 R2 is installed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="58527-127"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="58527-127"><dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="58527-128">已安裝終端機服務。</span><span class="sxs-lookup"><span data-stu-id="58527-128">Terminal Services is installed.</span></span> <span data-ttu-id="58527-129">一律會設定這個值。</span><span class="sxs-lookup"><span data-stu-id="58527-129">This value is always set.</span></span><br/> <span data-ttu-id="58527-130">如果已設定 **TerminalServer** ，但未設定 **SingleUserTS** ，則系統會在應用程式伺服器模式中執行。</span><span class="sxs-lookup"><span data-stu-id="58527-130">If **TerminalServer** is set but **SingleUserTS** is not set, the system is running in application server mode.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="58527-131"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="58527-131"><dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="58527-132">Microsoft Small Business Server 會以強制的嚴格用戶端授權安裝。</span><span class="sxs-lookup"><span data-stu-id="58527-132">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="58527-133">如需此位旗標的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="58527-133">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                                                            |
| <dl> <span data-ttu-id="58527-134"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="58527-134"><dt>0x00000040</dt></span></span> </dl> | <span data-ttu-id="58527-135">已安裝 Windows XP Embedded。</span><span class="sxs-lookup"><span data-stu-id="58527-135">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="58527-136"><dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="58527-136"><dt>0x00000080</dt></span></span> </dl> | <span data-ttu-id="58527-137">已安裝 windows Server 2008 Datacenter、Windows Server 2003、Datacenter Edition 或 Windows 2000 Datacenter Server。</span><span class="sxs-lookup"><span data-stu-id="58527-137">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="58527-138"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="58527-138"><dt>0x00000100</dt></span></span> </dl> | <span data-ttu-id="58527-139">支援遠端桌面，但只支援一個互動式會話。</span><span class="sxs-lookup"><span data-stu-id="58527-139">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="58527-140">除非系統是在應用程式伺服器模式中執行，否則會設定此值。</span><span class="sxs-lookup"><span data-stu-id="58527-140">This value is set unless the system is running in application server mode.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="58527-141"><dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="58527-141"><dt>0x00000200</dt></span></span> </dl> | <span data-ttu-id="58527-142">已安裝 windows Vista Home Premium、Windows Vista Home Basic 或 Windows XP Home Edition。</span><span class="sxs-lookup"><span data-stu-id="58527-142">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="58527-143"><dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="58527-143"><dt>0x00000400</dt></span></span> </dl> | <span data-ttu-id="58527-144">已安裝 Windows Server 2003 （Web Edition）。</span><span class="sxs-lookup"><span data-stu-id="58527-144">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="58527-145"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="58527-145"><dt>0x00002000</dt></span></span> </dl> | <span data-ttu-id="58527-146">已安裝 windows Storage Server 2003 R2 或 Windows Storage Server 2003。</span><span class="sxs-lookup"><span data-stu-id="58527-146">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="58527-147"><dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="58527-147"><dt>0x00004000</dt></span></span> </dl> | <span data-ttu-id="58527-148">已安裝 Windows Server 2003、Compute Cluster Edition。</span><span class="sxs-lookup"><span data-stu-id="58527-148">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="58527-149"><dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="58527-149"><dt>0x00008000</dt></span></span> </dl> | <span data-ttu-id="58527-150">已安裝 Windows Home Server。</span><span class="sxs-lookup"><span data-stu-id="58527-150">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="58527-151">備註</span><span class="sxs-lookup"><span data-stu-id="58527-151">Remarks</span></span>

<span data-ttu-id="58527-152">您不應該只依賴0x00000001 旗標來判斷系統上是否已安裝 Small Business Server，因為此旗標和0x00000020 旗標都是在安裝此產品套件時所設定。</span><span class="sxs-lookup"><span data-stu-id="58527-152">You should not rely upon only the 0x00000001 flag to determine whether Small Business Server has been installed on the system, as both this flag and the 0x00000020 flag are set when this product suite is installed.</span></span> <span data-ttu-id="58527-153">如果您將此安裝升級至 Windows Server Standard Edition，則會清除0x00000020 旗標，但會保持設定0x00000001 旗標。</span><span class="sxs-lookup"><span data-stu-id="58527-153">If you upgrade this installation to Windows Server, Standard Edition, the 0x00000020 flag will be cleared however, the 0x00000001 flag will remain set.</span></span> <span data-ttu-id="58527-154">在此情況下，這表示此系統上已安裝 Small Business Server。</span><span class="sxs-lookup"><span data-stu-id="58527-154">In this case, this indicates that Small Business Server was once installed on this system.</span></span> <span data-ttu-id="58527-155">如果此安裝進一步升級為 Windows Server Enterprise Edition，則會維持設定0x00000001 旗標。</span><span class="sxs-lookup"><span data-stu-id="58527-155">If this installation is further upgraded to Windows Server, Enterprise Edition, the 0x00000001 flag will remain set.</span></span>

## <a name="requirements"></a><span data-ttu-id="58527-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="58527-156">Requirements</span></span>



| <span data-ttu-id="58527-157">需求</span><span class="sxs-lookup"><span data-stu-id="58527-157">Requirement</span></span> | <span data-ttu-id="58527-158">值</span><span class="sxs-lookup"><span data-stu-id="58527-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="58527-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58527-159">Minimum supported client</span></span><br/> | <span data-ttu-id="58527-160">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58527-160">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="58527-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58527-161">Minimum supported server</span></span><br/> | <span data-ttu-id="58527-162">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58527-162">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="58527-163">標頭</span><span class="sxs-lookup"><span data-stu-id="58527-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="58527-164"><dt>Ntddk。h</dt></span><span class="sxs-lookup"><span data-stu-id="58527-164"><dt>Ntddk.h</dt></span></span> </dl>   |
| <span data-ttu-id="58527-165">程式庫</span><span class="sxs-lookup"><span data-stu-id="58527-165">Library</span></span><br/>                  | <dl> <span data-ttu-id="58527-166"><dt>Ntdll.dll .lib</dt></span><span class="sxs-lookup"><span data-stu-id="58527-166"><dt>Ntdll.lib</dt></span></span> </dl> |
| <span data-ttu-id="58527-167">DLL</span><span class="sxs-lookup"><span data-stu-id="58527-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58527-168"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58527-168"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




