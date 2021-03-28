---
description: 設定指派給連結的圖示位置。
ms.assetid: 257bb8e2-29fa-4d2f-ac2d-3497cf12959c
title: 'ShellLinkObject. SetIconLocation 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.SetIconLocation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 996f9648e9b9f59e1e84871abac1d6b37e2592d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991678"
---
# <a name="shelllinkobjectseticonlocation-method"></a><span data-ttu-id="0ca48-103">ShellLinkObject. SetIconLocation 方法</span><span class="sxs-lookup"><span data-stu-id="0ca48-103">ShellLinkObject.SetIconLocation method</span></span>

<span data-ttu-id="0ca48-104">設定指派給連結的圖示位置。</span><span class="sxs-lookup"><span data-stu-id="0ca48-104">Sets the location of the icon assigned to the link.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca48-105">語法</span><span class="sxs-lookup"><span data-stu-id="0ca48-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.SetIconLocation(
  sPath,
  iIndex
)
```



## <a name="parameters"></a><span data-ttu-id="0ca48-106">參數</span><span class="sxs-lookup"><span data-stu-id="0ca48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ca48-107">*sPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0ca48-107">*sPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca48-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="0ca48-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="0ca48-109">包含圖示之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0ca48-109">The fully qualified path of the file that contains the icon.</span></span>

</dd> <dt>

<span data-ttu-id="0ca48-110">*iIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0ca48-110">*iIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca48-111">類型： **整數**</span><span class="sxs-lookup"><span data-stu-id="0ca48-111">Type: **Integer**</span></span>

<span data-ttu-id="0ca48-112">*SPath* 所指定檔案中的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="0ca48-112">The index of the icon in the file specified by *sPath*.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="0ca48-113">範例</span><span class="sxs-lookup"><span data-stu-id="0ca48-113">Examples</span></span>

<span data-ttu-id="0ca48-114">下列範例會示範如何適當地使用此方法來進行 JScript、VBScript 和 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="0ca48-114">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0ca48-115">Jscript：</span><span class="sxs-lookup"><span data-stu-id="0ca48-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectSetIconLocationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.SetIconLocation(objShellLink.Path, 1);
                    objShellLink.Save();
                }
            }
        }
    }
</script>
```



<span data-ttu-id="0ca48-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="0ca48-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectSetIconLocationVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.SetIconLocation objShellLink.Path, 1
                                objShellLink.Save
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="0ca48-117">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="0ca48-117">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectSetIconLocationVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.SetIconLocation objShellLink.Path, 1
                            objShellLink.Save
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0ca48-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ca48-118">Requirements</span></span>



| <span data-ttu-id="0ca48-119">需求</span><span class="sxs-lookup"><span data-stu-id="0ca48-119">Requirement</span></span> | <span data-ttu-id="0ca48-120">值</span><span class="sxs-lookup"><span data-stu-id="0ca48-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca48-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ca48-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0ca48-122">僅限 Windows 2000 Professional 含 SP3 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ca48-122">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0ca48-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ca48-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0ca48-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ca48-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0ca48-125">標頭</span><span class="sxs-lookup"><span data-stu-id="0ca48-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ca48-126"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ca48-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="0ca48-127">Idl</span><span class="sxs-lookup"><span data-stu-id="0ca48-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ca48-128"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ca48-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="0ca48-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0ca48-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ca48-130"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="0ca48-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
