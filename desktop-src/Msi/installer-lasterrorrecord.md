---
description: 安裝程式物件的 LastErrorRecord 方法會傳回記錄物件，其中包含產生錯誤記錄之函式的最新錯誤的錯誤參數。
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: LastErrorRecord 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b368f30b04734b2d253a7d5f2aa64f0d61c930e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976554"
---
# <a name="installerlasterrorrecord-method"></a><span data-ttu-id="ca279-103">LastErrorRecord 方法</span><span class="sxs-lookup"><span data-stu-id="ca279-103">Installer.LastErrorRecord method</span></span>

<span data-ttu-id="ca279-104">[**安裝程式**](installer-object.md)物件的 **LastErrorRecord** 方法會傳回 [**記錄**](record-object.md)物件，其中包含產生錯誤記錄之函式的最新錯誤的錯誤參數。</span><span class="sxs-lookup"><span data-stu-id="ca279-104">The **LastErrorRecord** method of the [**Installer**](installer-object.md) object returns a [**Record**](record-object.md) object that contains error parameters for the most recent error from the function that produced the error record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca279-105">語法</span><span class="sxs-lookup"><span data-stu-id="ca279-105">Syntax</span></span>


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a><span data-ttu-id="ca279-106">參數</span><span class="sxs-lookup"><span data-stu-id="ca279-106">Parameters</span></span>

<span data-ttu-id="ca279-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ca279-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca279-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ca279-108">Return value</span></span>

<span data-ttu-id="ca279-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ca279-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca279-110">備註</span><span class="sxs-lookup"><span data-stu-id="ca279-110">Remarks</span></span>

<span data-ttu-id="ca279-111">在任何產生錯誤記錄的函式執行此函數之後，會重設 [**記錄**](record-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ca279-111">The [**Record**](record-object.md) object is reset after the execution of this function of any function that generates an error record.</span></span>

<span data-ttu-id="ca279-112">只有下列指定的函式會產生錯誤記錄：</span><span class="sxs-lookup"><span data-stu-id="ca279-112">Only the following designated functions generate an error record:</span></span>

-   [<span data-ttu-id="ca279-113">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="ca279-113">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="ca279-114">**Commit**</span><span class="sxs-lookup"><span data-stu-id="ca279-114">**Commit**</span></span>](database-commit.md)
-   [<span data-ttu-id="ca279-115">**OpenView**</span><span class="sxs-lookup"><span data-stu-id="ca279-115">**OpenView**</span></span>](database-openview.md)
-   [<span data-ttu-id="ca279-116">**匯入**</span><span class="sxs-lookup"><span data-stu-id="ca279-116">**Import**</span></span>](database-import.md)
-   [<span data-ttu-id="ca279-117">**出口**</span><span class="sxs-lookup"><span data-stu-id="ca279-117">**Export**</span></span>](database-export.md)
-   [<span data-ttu-id="ca279-118">**合併**</span><span class="sxs-lookup"><span data-stu-id="ca279-118">**Merge**</span></span>](database-merge.md)
-   [<span data-ttu-id="ca279-119">**基表**</span><span class="sxs-lookup"><span data-stu-id="ca279-119">**GenerateTransform**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="ca279-120">**ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="ca279-120">**ApplyTransform**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="ca279-121">**執行**</span><span class="sxs-lookup"><span data-stu-id="ca279-121">**Execute**</span></span>](view-execute.md)
-   [<span data-ttu-id="ca279-122">**修改**</span><span class="sxs-lookup"><span data-stu-id="ca279-122">**Modify**</span></span>](view-modify.md)
-   [<span data-ttu-id="ca279-123">**SetStream**</span><span class="sxs-lookup"><span data-stu-id="ca279-123">**SetStream**</span></span>](record-setstream.md)
-   [<span data-ttu-id="ca279-124">**SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="ca279-124">**SummaryInformation**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="ca279-125">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="ca279-125">**SourcePath**</span></span>](session-sourcepath.md)
-   [<span data-ttu-id="ca279-126">**TargetPath**</span><span class="sxs-lookup"><span data-stu-id="ca279-126">**TargetPath**</span></span>](session-targetpath.md)
-   [<span data-ttu-id="ca279-127">**ComponentCurrentState**</span><span class="sxs-lookup"><span data-stu-id="ca279-127">**ComponentCurrentState**</span></span>](session-componentcurrentstate.md)
-   [<span data-ttu-id="ca279-128">**ComponentRequestState**</span><span class="sxs-lookup"><span data-stu-id="ca279-128">**ComponentRequestState**</span></span>](session-componentrequeststate.md)
-   [<span data-ttu-id="ca279-129">**FeatureCurrentState**</span><span class="sxs-lookup"><span data-stu-id="ca279-129">**FeatureCurrentState**</span></span>](session-featurecurrentstate.md)
-   [<span data-ttu-id="ca279-130">**FeatureRequestState**</span><span class="sxs-lookup"><span data-stu-id="ca279-130">**FeatureRequestState**</span></span>](session-featurerequeststate.md)
-   [<span data-ttu-id="ca279-131">**FeatureCost**</span><span class="sxs-lookup"><span data-stu-id="ca279-131">**FeatureCost**</span></span>](session-featurecost.md)
-   [<span data-ttu-id="ca279-132">**FeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="ca279-132">**FeatureValidStates**</span></span>](session-featurevalidstates.md)
-   [<span data-ttu-id="ca279-133">**SetInstallLevel**</span><span class="sxs-lookup"><span data-stu-id="ca279-133">**SetInstallLevel**</span></span>](session-setinstalllevel.md)

<span data-ttu-id="ca279-134">VBScript 中的下列範例會使用 [**OpenDatabase**](installer-opendatabase.md) 的呼叫，以示範如何從支援 **LastErrorRecord** 方法的其中一個方法或屬性取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="ca279-134">The following sample in VBScript uses a call to [**OpenDatabase**](installer-opendatabase.md) to show how to obtain extended error information from one of the methods or properties that support the **LastErrorRecord** method.</span></span> <span data-ttu-id="ca279-135">當 **OpenDatabase** 方法失敗時，此範例會建立錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="ca279-135">The sample constructs an error message when the **OpenDatabase** method fails.</span></span> <span data-ttu-id="ca279-136">**Err** 物件是用來判斷是否發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ca279-136">The **Err** object is used to determine whether an error was encountered.</span></span>


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a><span data-ttu-id="ca279-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca279-137">Requirements</span></span>



| <span data-ttu-id="ca279-138">需求</span><span class="sxs-lookup"><span data-stu-id="ca279-138">Requirement</span></span> | <span data-ttu-id="ca279-139">值</span><span class="sxs-lookup"><span data-stu-id="ca279-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca279-140">版本</span><span class="sxs-lookup"><span data-stu-id="ca279-140">Version</span></span><br/> | <span data-ttu-id="ca279-141">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="ca279-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ca279-142">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="ca279-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ca279-143">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ca279-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ca279-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ca279-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="ca279-145"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca279-145"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ca279-146">IID</span><span class="sxs-lookup"><span data-stu-id="ca279-146">IID</span></span><br/>     | <span data-ttu-id="ca279-147">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ca279-147">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




