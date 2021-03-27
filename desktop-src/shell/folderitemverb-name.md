---
description: 包含動詞的名稱。
ms.assetid: d18fddac-eb51-4031-a572-1bfef2f757a9
title: 'FolderItemVerb.Name 屬性 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.Name
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5d352f02486f1d7304d4c474aa836401bfef635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971872"
---
# <a name="folderitemverbname-property"></a><span data-ttu-id="5455d-103">FolderItemVerb.Name 屬性</span><span class="sxs-lookup"><span data-stu-id="5455d-103">FolderItemVerb.Name property</span></span>

<span data-ttu-id="5455d-104">包含動詞的名稱。</span><span class="sxs-lookup"><span data-stu-id="5455d-104">Contains the verb's name.</span></span>

<span data-ttu-id="5455d-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5455d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5455d-106">語法</span><span class="sxs-lookup"><span data-stu-id="5455d-106">Syntax</span></span>


```JScript
strName = FolderItemVerb.Name
```



## <a name="property-value"></a><span data-ttu-id="5455d-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="5455d-107">Property value</span></span>

<span data-ttu-id="5455d-108">可接收 Name 屬性之 [**BSTR**](/previous-versions/windows/desktop/automat/bstr) 類型的變數。</span><span class="sxs-lookup"><span data-stu-id="5455d-108">A variable of type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) that receives the Name property.</span></span>

## <a name="examples"></a><span data-ttu-id="5455d-109">範例</span><span class="sxs-lookup"><span data-stu-id="5455d-109">Examples</span></span>

<span data-ttu-id="5455d-110">下列範例會使用 **名稱** ，在使用者的程式資料夾回應的動詞集合中取出第一個專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="5455d-110">The following example uses **Name** to retrieve the name of the first item in the collection of verbs to which the user's Program folder responds.</span></span> <span data-ttu-id="5455d-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="5455d-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5455d-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="5455d-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbNameJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objVerbs;
            
            objVerbs = objFolder.Self.Verbs();
            if (objVerbs != null)
            {
                var szReturn = "";
                
                szReturn = objVerbs.Item(0).Name;
                alert(szReturn);
            }
        }
    }
</script>
```



<span data-ttu-id="5455d-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="5455d-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbNameVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objVerbs
                
                set objVerbs = objFolder.Self.Verbs
                    if (not objVerbs is nothing) then
                        dim szReturn
                        
                        szReturn = objVerbs.Item(0).Name
                        alert(szReturn)
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="5455d-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="5455d-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbNameVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        
        Set objVerbs = objFolder2.Self.Verbs
            If (Not objVerbs Is Nothing) Then
                Dim szReturn As String
                
                szReturn = objVerbs.Item(0).Name
                Debug.Print szReturn
            End If
        Set objVerbs = Nothing
    End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5455d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5455d-115">Requirements</span></span>



| <span data-ttu-id="5455d-116">需求</span><span class="sxs-lookup"><span data-stu-id="5455d-116">Requirement</span></span> | <span data-ttu-id="5455d-117">值</span><span class="sxs-lookup"><span data-stu-id="5455d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5455d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5455d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5455d-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5455d-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5455d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5455d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5455d-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5455d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5455d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5455d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5455d-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="5455d-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5455d-124">Idl</span><span class="sxs-lookup"><span data-stu-id="5455d-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5455d-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5455d-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5455d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5455d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5455d-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="5455d-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
