---
description: 抓取集合中指定之專案的 FolderItemVerb 物件。
ms.assetid: 65871926-0920-4ad6-82da-7aba0a3c0fab
title: 'FolderItemVerbs 專案方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 013215af3f5005e68b396312d0ef13fa974d8a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973201"
---
# <a name="folderitemverbsitem-method"></a><span data-ttu-id="1003c-103">FolderItemVerbs 專案方法</span><span class="sxs-lookup"><span data-stu-id="1003c-103">FolderItemVerbs.Item method</span></span>

<span data-ttu-id="1003c-104">抓取集合中指定之專案的 [**FolderItemVerb**](folderitemverb.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="1003c-104">Retrieves the [**FolderItemVerb**](folderitemverb.md) object for a specified item in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1003c-105">語法</span><span class="sxs-lookup"><span data-stu-id="1003c-105">Syntax</span></span>


```JScript
retVal = FolderItemVerbs.Item(
  iIndex
)
```



## <a name="parameters"></a><span data-ttu-id="1003c-106">參數</span><span class="sxs-lookup"><span data-stu-id="1003c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1003c-107">*iIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1003c-107">*iIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1003c-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="1003c-108">Type: **Variant**</span></span>

<span data-ttu-id="1003c-109">要擷取之項目的索引，此索引以零起始。</span><span class="sxs-lookup"><span data-stu-id="1003c-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="1003c-110">這個值必須小於 [**Count**](folderitemverbs-count.md) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1003c-110">This value must be less than the value of the [**Count**](folderitemverbs-count.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1003c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1003c-111">Return value</span></span>

<span data-ttu-id="1003c-112">類型： **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="1003c-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="1003c-113">接收 [**FolderItemVerb**](folderitemverb.md) 物件的物件。</span><span class="sxs-lookup"><span data-stu-id="1003c-113">Object that receives the [**FolderItemVerb**](folderitemverb.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="1003c-114">範例</span><span class="sxs-lookup"><span data-stu-id="1003c-114">Examples</span></span>

<span data-ttu-id="1003c-115">下列範例會使用 **專案** 來抓取集合中可供主控台資料夾使用的第一個動詞命令，並顯示其名稱。</span><span class="sxs-lookup"><span data-stu-id="1003c-115">The following example uses **Item** to retrieve the first verbs in the collection available to the Control Panel folder and displays its name.</span></span> <span data-ttu-id="1003c-116">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="1003c-116">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1003c-117">Jscript：</span><span class="sxs-lookup"><span data-stu-id="1003c-117">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);

        if (objFolder2 != null)
        {
            var objVerbs;
            objVerbs = objFolder2.Self.Verbs();
 
            if (objVerbs != null)
            {
                var objFolderItemVerb;
                objFolderItemVerb = objVerbs.Item(0);
 
                if (objFolderItemVerb != null)
                {
                    alert(objFolderItemVerb.Name);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="1003c-118">VBScript</span><span class="sxs-lookup"><span data-stu-id="1003c-118">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbsItemVB()
        dim objShell
        dim objFolder2
        dim ssfCONTROLS
        
        ssfCONTROLS = 3
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace(ssfCONTROLS)
        if (not objFolder2 is nothing) then
            dim objVerbs
            set objVerbs = objFolder2.Self.Verbs

            if (not objVerbs is nothing) then
                dim objFolderItemVerb
                set objFolderItemVerb = objVerbs.Item(0)

                if (not objFolderItemVerb is nothing) then
                    alert(objFolderItemVerb.Name)
                end if

                set objFolderItemVerb = nothing
            end if

            set objVerbs = nothing
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="1003c-119">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="1003c-119">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbsItemVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfCONTROLS As Long
            
    ssfCONTROLS = 3
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)

    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        Set objVerbs = objFolder2.Self.Verbs

        If (Not objVerbs Is Nothing) Then
            Dim objFolderItemVerb As FolderItemVerb
            Set objFolderItemVerb = objVerbs.Item(0)

            If (Not objFolderItemVerb Is Nothing) Then
                Debug.Print objFolderItemVerb.Name
            End If

            Set objFolderItemVerb = Nothing
        End If

        Set objVerbs = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1003c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1003c-120">Requirements</span></span>



| <span data-ttu-id="1003c-121">需求</span><span class="sxs-lookup"><span data-stu-id="1003c-121">Requirement</span></span> | <span data-ttu-id="1003c-122">值</span><span class="sxs-lookup"><span data-stu-id="1003c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1003c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1003c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1003c-124">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1003c-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1003c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1003c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1003c-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1003c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1003c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="1003c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1003c-128"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1003c-128"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1003c-129">Idl</span><span class="sxs-lookup"><span data-stu-id="1003c-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1003c-130"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1003c-130"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1003c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1003c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1003c-132"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="1003c-132"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
