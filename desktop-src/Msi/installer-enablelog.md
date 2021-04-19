---
description: 安裝程式物件的 EnableLog 方法，可針對目前進程空間中的所有後續安裝會話，記錄所選取的訊息類型。
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: EnableLog 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975747"
---
# <a name="installerenablelog-method"></a><span data-ttu-id="b7467-103">EnableLog 方法</span><span class="sxs-lookup"><span data-stu-id="b7467-103">Installer.EnableLog method</span></span>

<span data-ttu-id="b7467-104">[**安裝程式**](installer-object.md)物件的 **EnableLog** 方法，可針對目前進程空間中的所有後續安裝會話，記錄所選取的訊息類型。</span><span class="sxs-lookup"><span data-stu-id="b7467-104">The **EnableLog** method of the [**Installer**](installer-object.md) object enables logging of the selected message type for all subsequent installation sessions in the current process space.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7467-105">語法</span><span class="sxs-lookup"><span data-stu-id="b7467-105">Syntax</span></span>


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a><span data-ttu-id="b7467-106">參數</span><span class="sxs-lookup"><span data-stu-id="b7467-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7467-107">*logMode*</span><span class="sxs-lookup"><span data-stu-id="b7467-107">*logMode*</span></span> 
</dt> <dd>

<span data-ttu-id="b7467-108">必要的字串，其中包含代表要記錄之訊息類型的字母。</span><span class="sxs-lookup"><span data-stu-id="b7467-108">A required string that contains letters representing the message types to log.</span></span> <span data-ttu-id="b7467-109">字串可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="b7467-109">The string can be a combination of the following values.</span></span>



| <span data-ttu-id="b7467-110">值</span><span class="sxs-lookup"><span data-stu-id="b7467-110">Value</span></span> | <span data-ttu-id="b7467-111">描述</span><span class="sxs-lookup"><span data-stu-id="b7467-111">Description</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7467-112">I</span><span class="sxs-lookup"><span data-stu-id="b7467-112">I</span></span>     | <span data-ttu-id="b7467-113">僅限資訊的訊息。</span><span class="sxs-lookup"><span data-stu-id="b7467-113">Information-only messages.</span></span>                                                                             |
| <span data-ttu-id="b7467-114">w</span><span class="sxs-lookup"><span data-stu-id="b7467-114">w</span></span>     | <span data-ttu-id="b7467-115">非嚴重警告訊息。</span><span class="sxs-lookup"><span data-stu-id="b7467-115">Non-fatal warning messages.</span></span>                                                                            |
| <span data-ttu-id="b7467-116">e</span><span class="sxs-lookup"><span data-stu-id="b7467-116">e</span></span>     | <span data-ttu-id="b7467-117">可能是嚴重錯誤的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b7467-117">Error messages that may be fatal errors.</span></span>                                                               |
| <span data-ttu-id="b7467-118">f</span><span class="sxs-lookup"><span data-stu-id="b7467-118">f</span></span>     | <span data-ttu-id="b7467-119">使用中需要取代的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="b7467-119">List of files in use that need to be replaced.</span></span>                                                         |
| <span data-ttu-id="b7467-120">a</span><span class="sxs-lookup"><span data-stu-id="b7467-120">a</span></span>     | <span data-ttu-id="b7467-121">開始動作通知。</span><span class="sxs-lookup"><span data-stu-id="b7467-121">Start of action notification.</span></span>                                                                          |
| <span data-ttu-id="b7467-122">r</span><span class="sxs-lookup"><span data-stu-id="b7467-122">r</span></span>     | <span data-ttu-id="b7467-123">動作資料記錄，其中包含動作特定的內容。</span><span class="sxs-lookup"><span data-stu-id="b7467-123">Action data record containing content specific to action.</span></span>                                              |
| <span data-ttu-id="b7467-124">u</span><span class="sxs-lookup"><span data-stu-id="b7467-124">u</span></span>     | <span data-ttu-id="b7467-125">使用者要求訊息。</span><span class="sxs-lookup"><span data-stu-id="b7467-125">User request messages.</span></span>                                                                                 |
| <span data-ttu-id="b7467-126">c</span><span class="sxs-lookup"><span data-stu-id="b7467-126">c</span></span>     | <span data-ttu-id="b7467-127">UI 初始化參數。</span><span class="sxs-lookup"><span data-stu-id="b7467-127">UI initialization parameters.</span></span>                                                                          |
| <span data-ttu-id="b7467-128">m</span><span class="sxs-lookup"><span data-stu-id="b7467-128">m</span></span>     | <span data-ttu-id="b7467-129">記憶體不足的訊息。</span><span class="sxs-lookup"><span data-stu-id="b7467-129">Out-of-memory message.</span></span>                                                                                 |
| <span data-ttu-id="b7467-130">v</span><span class="sxs-lookup"><span data-stu-id="b7467-130">v</span></span>     | <span data-ttu-id="b7467-131">將大量資訊傳送至記錄檔，對使用者而言通常不實用。</span><span class="sxs-lookup"><span data-stu-id="b7467-131">Sends large amounts of information to log file not generally useful to users.</span></span> <span data-ttu-id="b7467-132">可以用來提供支援。</span><span class="sxs-lookup"><span data-stu-id="b7467-132">May be used for support.</span></span> |
| <span data-ttu-id="b7467-133">p</span><span class="sxs-lookup"><span data-stu-id="b7467-133">p</span></span>     | <span data-ttu-id="b7467-134">傾印屬性工作表;引擎終止時的 "property = value"</span><span class="sxs-lookup"><span data-stu-id="b7467-134">Dump property table; "property = value" at engine termination</span></span>                                          |
| \+    | <span data-ttu-id="b7467-135">附加至現有的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7467-135">Append to existing log file.</span></span>                                                                           |
| <span data-ttu-id="b7467-136">!</span><span class="sxs-lookup"><span data-stu-id="b7467-136">!</span></span>     | <span data-ttu-id="b7467-137">將每一行排清到記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7467-137">Flush each line to the log file.</span></span>                                                                       |
| <span data-ttu-id="b7467-138">x</span><span class="sxs-lookup"><span data-stu-id="b7467-138">x</span></span>     | <span data-ttu-id="b7467-139">額外的調試資訊。</span><span class="sxs-lookup"><span data-stu-id="b7467-139">Extra debugging information.</span></span> <span data-ttu-id="b7467-140">此選項僅適用于 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="b7467-140">This option only available with Windows Server 2003.</span></span>                      |
| <span data-ttu-id="b7467-141">o</span><span class="sxs-lookup"><span data-stu-id="b7467-141">o</span></span>     | <span data-ttu-id="b7467-142">磁碟空間不足的訊息。</span><span class="sxs-lookup"><span data-stu-id="b7467-142">Out-of-disk-space messages.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="b7467-143">*記錄檔*</span><span class="sxs-lookup"><span data-stu-id="b7467-143">*logFile*</span></span> 
</dt> <dd>

<span data-ttu-id="b7467-144">必要的字串，其中包含要建立之記錄檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="b7467-144">Required string containing the path to the log file to be created.</span></span> <span data-ttu-id="b7467-145">使用空字串 ( "" ) 來關閉記錄。</span><span class="sxs-lookup"><span data-stu-id="b7467-145">Use an empty string ("") to turn off logging.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7467-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7467-146">Return value</span></span>

<span data-ttu-id="b7467-147">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b7467-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7467-148">備註</span><span class="sxs-lookup"><span data-stu-id="b7467-148">Remarks</span></span>

<span data-ttu-id="b7467-149">使用這個方法時，記錄檔位置的路徑必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="b7467-149">The path to the logfile location must already exist when using this method.</span></span> <span data-ttu-id="b7467-150">安裝程式不會建立記錄檔的目錄結構。</span><span class="sxs-lookup"><span data-stu-id="b7467-150">The Installer does not create the directory structure for the logfile.</span></span>

<span data-ttu-id="b7467-151">使用 **EnableLog** 所設定的記錄選項會覆寫任何現有的 Windows Installer 記錄原則設定。</span><span class="sxs-lookup"><span data-stu-id="b7467-151">The logging options set using **EnableLog** override any existing Windows Installer logging policy settings.</span></span>

<span data-ttu-id="b7467-152">記錄預設會覆寫現有的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7467-152">Logging overwrites an existing log file by default.</span></span> <span data-ttu-id="b7467-153">您必須在記錄模式中使用 ' + ' 字母，以附加至現有的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7467-153">You must use the '+' letter in the logging mode to append to an existing log file.</span></span>

<span data-ttu-id="b7467-154">不建議使用 '！ ' 選項，因為它可能會大幅降低安裝速度。</span><span class="sxs-lookup"><span data-stu-id="b7467-154">The '!' option is not recommended because it can significantly slow installation.</span></span> <span data-ttu-id="b7467-155">在對安裝進行偵錯工具時，此選項可能很有用。</span><span class="sxs-lookup"><span data-stu-id="b7467-155">This option may be useful when debugging an installation.</span></span>

<span data-ttu-id="b7467-156">下列範例腳本會開啟安裝的詳細資訊記錄。</span><span class="sxs-lookup"><span data-stu-id="b7467-156">The following sample script turns on verbose logging for an installation.</span></span> <span data-ttu-id="b7467-157">在安裝結束時，產生的記錄檔將會是 c： \\ temp \\ install .log。</span><span class="sxs-lookup"><span data-stu-id="b7467-157">At the end of the installation, the generated log file will be at c:\\temp\\install.log.</span></span>


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a><span data-ttu-id="b7467-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7467-158">Requirements</span></span>



| <span data-ttu-id="b7467-159">需求</span><span class="sxs-lookup"><span data-stu-id="b7467-159">Requirement</span></span> | <span data-ttu-id="b7467-160">值</span><span class="sxs-lookup"><span data-stu-id="b7467-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7467-161">版本</span><span class="sxs-lookup"><span data-stu-id="b7467-161">Version</span></span><br/> | <span data-ttu-id="b7467-162">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="b7467-162">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b7467-163">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="b7467-163">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b7467-164">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="b7467-164">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b7467-165">DLL</span><span class="sxs-lookup"><span data-stu-id="b7467-165">DLL</span></span><br/>     | <dl> <span data-ttu-id="b7467-166"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7467-166"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b7467-167">IID</span><span class="sxs-lookup"><span data-stu-id="b7467-167">IID</span></span><br/>     | <span data-ttu-id="b7467-168">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b7467-168">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="b7467-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7467-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7467-170">Windows Installer 記錄</span><span class="sxs-lookup"><span data-stu-id="b7467-170">Windows Installer Logging</span></span>](windows-installer-logging.md)
</dt> </dl>

 

 




