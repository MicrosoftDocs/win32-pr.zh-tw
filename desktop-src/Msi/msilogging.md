---
description: MsiLogging 屬性會設定 Windows Installer 封裝的預設記錄模式。
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: MsiLogging 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995478"
---
# <a name="msilogging-property"></a><span data-ttu-id="a990e-103">MsiLogging 屬性</span><span class="sxs-lookup"><span data-stu-id="a990e-103">MsiLogging property</span></span>

<span data-ttu-id="a990e-104">**MsiLogging** 屬性會設定 Windows Installer 封裝的預設記錄模式。</span><span class="sxs-lookup"><span data-stu-id="a990e-104">The **MsiLogging** property sets the default logging mode for the Windows Installer package.</span></span> <span data-ttu-id="a990e-105">如果這個選擇性屬性存在於 [屬性工作表](property-table.md)中，安裝程式會產生名為 MSI 的記錄檔 \* 。日誌。</span><span class="sxs-lookup"><span data-stu-id="a990e-105">If this optional property is present in the [Property table](property-table.md), the installer generates a log file named MSI\*.LOG.</span></span> <span data-ttu-id="a990e-106">記錄檔的完整路徑是由 [**MsiLogFileLocation**](msilogfilelocation.md) 屬性的值提供。</span><span class="sxs-lookup"><span data-stu-id="a990e-106">The full path to the log file is given by the value of the [**MsiLogFileLocation**](msilogfilelocation.md) property.</span></span>

## <a name="value"></a><span data-ttu-id="a990e-107">值</span><span class="sxs-lookup"><span data-stu-id="a990e-107">Value</span></span>

<span data-ttu-id="a990e-108">這個屬性的值應該是下列字元的字串，指定預設的記錄模式。</span><span class="sxs-lookup"><span data-stu-id="a990e-108">The value of this property should be a string of the following characters that specify the default logging mode.</span></span>



| <span data-ttu-id="a990e-109">值</span><span class="sxs-lookup"><span data-stu-id="a990e-109">Value</span></span>                                                                        | <span data-ttu-id="a990e-110">意義</span><span class="sxs-lookup"><span data-stu-id="a990e-110">Meaning</span></span>                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a990e-111"><dt>我</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-111"><dt>I</dt></span></span> </dl> | <span data-ttu-id="a990e-112">狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="a990e-112">Status messages.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="a990e-113"><dt>w</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-113"><dt>w</dt></span></span> </dl> | <span data-ttu-id="a990e-114">非嚴重警告。</span><span class="sxs-lookup"><span data-stu-id="a990e-114">Nonfatal warnings.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="a990e-115"><dt>pci-e</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-115"><dt>e</dt></span></span> </dl> | <span data-ttu-id="a990e-116">所有錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="a990e-116">All error messages.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="a990e-117"><dt>的</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-117"><dt>a</dt></span></span> </dl> | <span data-ttu-id="a990e-118">啟動動作。</span><span class="sxs-lookup"><span data-stu-id="a990e-118">Start up of actions.</span></span><br/>                                                |
| <dl> <span data-ttu-id="a990e-119"><dt>r</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-119"><dt>r</dt></span></span> </dl> | <span data-ttu-id="a990e-120">動作特定記錄。</span><span class="sxs-lookup"><span data-stu-id="a990e-120">Action-specific records.</span></span><br/>                                            |
| <dl> <span data-ttu-id="a990e-121"><dt>u</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-121"><dt>u</dt></span></span> </dl> | <span data-ttu-id="a990e-122">使用者要求。</span><span class="sxs-lookup"><span data-stu-id="a990e-122">User requests.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="a990e-123"><dt>c</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-123"><dt>c</dt></span></span> </dl> | <span data-ttu-id="a990e-124">初始 UI 參數。</span><span class="sxs-lookup"><span data-stu-id="a990e-124">Initial UI parameters.</span></span><br/>                                              |
| <dl> <span data-ttu-id="a990e-125"><dt>m</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-125"><dt>m</dt></span></span> </dl> | <span data-ttu-id="a990e-126">記憶體不足或嚴重的離開資訊。</span><span class="sxs-lookup"><span data-stu-id="a990e-126">Out-of-memory or fatal exit information.</span></span><br/>                            |
| <dl> <span data-ttu-id="a990e-127"><dt>o</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-127"><dt>o</dt></span></span> </dl> | <span data-ttu-id="a990e-128">磁碟空間不足的訊息。</span><span class="sxs-lookup"><span data-stu-id="a990e-128">Out-of-disk-space messages.</span></span><br/>                                         |
| <dl> <span data-ttu-id="a990e-129"><dt>P</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-129"><dt>p</dt></span></span> </dl> | <span data-ttu-id="a990e-130">終端機屬性。</span><span class="sxs-lookup"><span data-stu-id="a990e-130">Terminal properties.</span></span><br/>                                                |
| <dl> <span data-ttu-id="a990e-131"><dt>V</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-131"><dt>v</dt></span></span> </dl> | <span data-ttu-id="a990e-132">詳細資訊輸出。</span><span class="sxs-lookup"><span data-stu-id="a990e-132">Verbose output.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="a990e-133"><dt>x</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-133"><dt>x</dt></span></span> </dl> | <span data-ttu-id="a990e-134">額外的調試資訊。</span><span class="sxs-lookup"><span data-stu-id="a990e-134">Extra debugging information.</span></span> <span data-ttu-id="a990e-135">僅適用于 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="a990e-135">Only available on Windows Server 2003.</span></span><br/> |
| <dl> <span data-ttu-id="a990e-136"><dt>!</dt></span><span class="sxs-lookup"><span data-stu-id="a990e-136"><dt>!</dt></span></span> </dl> | <span data-ttu-id="a990e-137">將每一行排清到記錄檔。</span><span class="sxs-lookup"><span data-stu-id="a990e-137">Flush each line to the log.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="a990e-138">備註</span><span class="sxs-lookup"><span data-stu-id="a990e-138">Remarks</span></span>

<span data-ttu-id="a990e-139">從 Windows Installer 4.0 開始，可以使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="a990e-139">This property is available starting with Windows Installer 4.0.</span></span>

<span data-ttu-id="a990e-140">您無法 \* 在 **MsiLogging** 屬性的值中使用/l 選項的 "+" 和 "" 值。</span><span class="sxs-lookup"><span data-stu-id="a990e-140">You cannot use the "+" and "\*" values of the /L option in the value of the **MsiLogging** property.</span></span>

<span data-ttu-id="a990e-141">您可以使用原則、命令列選項或以程式設計方式來設定記錄模式。</span><span class="sxs-lookup"><span data-stu-id="a990e-141">The logging mode can be set using policy, a command-line option, or programmatically.</span></span> <span data-ttu-id="a990e-142">這會覆寫預設的記錄模式。</span><span class="sxs-lookup"><span data-stu-id="a990e-142">This overrides the default logging mode.</span></span> <span data-ttu-id="a990e-143">如需可用於設定記錄模式之所有方法的詳細資訊，請參閱[Windows Installer 記錄](windows-installer-logging.md)] 區段中的[一般記錄](normal-logging.md)。</span><span class="sxs-lookup"><span data-stu-id="a990e-143">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="a990e-144">如果 [屬性工作表](property-table.md)中有 **MsiLogging** 屬性，則可以使用 [資料庫轉換](database-transforms.md)來變更這個屬性的值，藉以修改封裝的預設記錄模式。</span><span class="sxs-lookup"><span data-stu-id="a990e-144">If the **MsiLogging** property is present in the [Property table](property-table.md), the default logging mode of the package can be modified by changing the value of this property using a [database transform](database-transforms.md).</span></span> <span data-ttu-id="a990e-145">無法使用 (.msp 檔的 [修補套件](patch-packages.md) 來變更預設記錄模式。 ) </span><span class="sxs-lookup"><span data-stu-id="a990e-145">The default logging mode cannot be changed using a [Patch Package](patch-packages.md) (a .msp file.)</span></span>

<span data-ttu-id="a990e-146">如果已在 [屬性工作表](property-table.md)中設定 **MsiLogging** 屬性，則可以藉由設定 [DisableLoggingFromPackage](disableloggingfrompackage.md)原則和 [記錄](logging.md)原則來指定電腦上所有使用者的預設記錄模式。</span><span class="sxs-lookup"><span data-stu-id="a990e-146">If the **MsiLogging** property has been set in the [Property table](property-table.md), the default logging mode for all users of the computer can be specified by setting both the [DisableLoggingFromPackage](disableloggingfrompackage.md) policy and [Logging](logging.md) policy.</span></span> <span data-ttu-id="a990e-147">同時設定 DisableLoggingFromPackage 原則和記錄原則，將會覆寫所有封裝的 **MsiLogging** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a990e-147">Setting both the DisableLoggingFromPackage policy and Logging policy will override the **MsiLogging** property for all packages.</span></span>

## <a name="requirements"></a><span data-ttu-id="a990e-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="a990e-148">Requirements</span></span>



| <span data-ttu-id="a990e-149">需求</span><span class="sxs-lookup"><span data-stu-id="a990e-149">Requirement</span></span> | <span data-ttu-id="a990e-150">值</span><span class="sxs-lookup"><span data-stu-id="a990e-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a990e-151">版本</span><span class="sxs-lookup"><span data-stu-id="a990e-151">Version</span></span><br/> | <span data-ttu-id="a990e-152">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="a990e-152">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a990e-153">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="a990e-153">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a990e-154">Windows Server 2003 或 Windows XP 上的 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="a990e-154">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a990e-155">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="a990e-155">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a990e-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a990e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a990e-157">屬性</span><span class="sxs-lookup"><span data-stu-id="a990e-157">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="a990e-158">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="a990e-158">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




