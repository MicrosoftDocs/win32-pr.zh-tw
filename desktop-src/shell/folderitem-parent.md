---
description: 取得物件，該物件表示專案的父系。
ms.assetid: 612e76d8-d8bc-419c-b319-75b1f324840a
title: 'FolderItem： Parent 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f2da3504596c3b351318b33c929dad3b5a958165
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689259"
---
# <a name="folderitemparent-property"></a><span data-ttu-id="8d314-103">FolderItem 父系屬性</span><span class="sxs-lookup"><span data-stu-id="8d314-103">FolderItem.Parent property</span></span>

<span data-ttu-id="8d314-104">取得物件，該物件表示專案的父系。</span><span class="sxs-lookup"><span data-stu-id="8d314-104">Gets an object that represents the parent of the item.</span></span>

<span data-ttu-id="8d314-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="8d314-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d314-106">語法</span><span class="sxs-lookup"><span data-stu-id="8d314-106">Syntax</span></span>


```JScript
objParent = FolderItem.Parent
```



## <a name="property-value"></a><span data-ttu-id="8d314-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="8d314-107">Property value</span></span>

<span data-ttu-id="8d314-108">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，可接收父物件。</span><span class="sxs-lookup"><span data-stu-id="8d314-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="examples"></a><span data-ttu-id="8d314-109">範例</span><span class="sxs-lookup"><span data-stu-id="8d314-109">Examples</span></span>

<span data-ttu-id="8d314-110">下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **父系** 。</span><span class="sxs-lookup"><span data-stu-id="8d314-110">The following example shows the proper use of **Parent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8d314-111">Jscript：</span><span class="sxs-lookup"><span data-stu-id="8d314-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



<span data-ttu-id="8d314-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="8d314-112">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnFolderItemParentVB()
        dim objShell
        dim objFolder2
        dim ssfWINDOWS

        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem

                set objFolderItem = objFolder2.Self
                    if (not objFolderItem is nothing) then
                        dim objParent

                        set objParent = objFolderItem.Parent
                            if (not objParent is nothing) then
                                alert("Got parent object")
                            end if
                        set objParent = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder2 = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="8d314-113">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="8d314-113">Visual Basic:</span></span>


```VB
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



## <a name="requirements"></a><span data-ttu-id="8d314-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d314-114">Requirements</span></span>



| <span data-ttu-id="8d314-115">需求</span><span class="sxs-lookup"><span data-stu-id="8d314-115">Requirement</span></span> | <span data-ttu-id="8d314-116">值</span><span class="sxs-lookup"><span data-stu-id="8d314-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d314-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d314-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8d314-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d314-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8d314-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d314-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8d314-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d314-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8d314-121">標頭</span><span class="sxs-lookup"><span data-stu-id="8d314-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d314-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d314-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8d314-123">Idl</span><span class="sxs-lookup"><span data-stu-id="8d314-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8d314-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8d314-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8d314-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8d314-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d314-126"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="8d314-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
