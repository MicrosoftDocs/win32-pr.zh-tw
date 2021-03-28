---
description: 捕獲代表 Shell 視窗的 Microsoft-windows-ie-internetexplorer 物件。
ms.assetid: 32390f35-f83a-45d9-a240-282da7cb2b13
title: 'ShellWindows 專案方法 (Exdisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ccdb73deb1d97d9c6e1ad8c335db3c58d796a299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193161"
---
# <a name="shellwindowsitem-method"></a><span data-ttu-id="2e290-103">ShellWindows 專案方法</span><span class="sxs-lookup"><span data-stu-id="2e290-103">ShellWindows.Item method</span></span>

<span data-ttu-id="2e290-104">捕獲代表 Shell 視窗的 [**microsoft-windows-ie-internetexplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="2e290-104">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e290-105">語法</span><span class="sxs-lookup"><span data-stu-id="2e290-105">Syntax</span></span>


```JScript
retVal = ShellWindows.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="2e290-106">參數</span><span class="sxs-lookup"><span data-stu-id="2e290-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e290-107">*iIndex* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2e290-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2e290-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="2e290-108">Type: **Variant**</span></span>

<span data-ttu-id="2e290-109">要擷取之項目的索引，此索引以零起始。</span><span class="sxs-lookup"><span data-stu-id="2e290-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="2e290-110">這個值必須小於 [**Count**](shellwindows-count.md) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="2e290-110">This value must be less than the value of the [**Count**](shellwindows-count.md) property.</span></span> <span data-ttu-id="2e290-111">如果省略此值，則會使用預設值0。</span><span class="sxs-lookup"><span data-stu-id="2e290-111">If this value is omitted, a default value of 0 is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e290-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e290-112">Return value</span></span>

<span data-ttu-id="2e290-113">類型： **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="2e290-113">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="2e290-114">代表 Shell 視窗之 [**microsoft-windows-ie-internetexplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) 物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="2e290-114">An object reference to the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="examples"></a><span data-ttu-id="2e290-115">範例</span><span class="sxs-lookup"><span data-stu-id="2e290-115">Examples</span></span>

<span data-ttu-id="2e290-116">下列範例會使用 [**專案**](folderitemverbs-item.md) 來取出代表第一個 Shell 視窗專案的 [**microsoft-windows-ie-internetexplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="2e290-116">The following example uses [**Item**](folderitemverbs-item.md) to retrieve the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the first Shell window item.</span></span> <span data-ttu-id="2e290-117">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="2e290-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2e290-118">Jscript：</span><span class="sxs-lookup"><span data-stu-id="2e290-118">JScript:</span></span>


```JavaScript
<script language="JScript">
    function fnShellWindowsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();
        if (objShellWindows != null)
        {
            var objIE;
            objIE = objShellWindows.Item();

            if (objIE != null)
            {
                alert(objIE.path());
            }
        }
    }
</script>
```



<span data-ttu-id="2e290-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="2e290-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsItemVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows()

        if (not objShellWindows is nothing) then
            dim objIE
            set objIE = objShellWindows.Item

            if (not objIE is nothing) then
                Wscript.Echo objIE.path
            end if

            set objIE = nothing
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2e290-120">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="2e290-120">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsItemVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows()

    If (Not objShellWindows Is Nothing) Then
        Dim objIE As InternetExplorer
        Set objIE = objShellWindows.Item

        If (Not objIE Is Nothing) Then
            Debug.Print objIE.Path
        End If

        Set objIE = Nothing
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2e290-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e290-121">Requirements</span></span>



| <span data-ttu-id="2e290-122">需求</span><span class="sxs-lookup"><span data-stu-id="2e290-122">Requirement</span></span> | <span data-ttu-id="2e290-123">值</span><span class="sxs-lookup"><span data-stu-id="2e290-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e290-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e290-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2e290-125">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e290-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2e290-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e290-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2e290-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e290-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2e290-128">標頭</span><span class="sxs-lookup"><span data-stu-id="2e290-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e290-129"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e290-129"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="2e290-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2e290-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e290-131"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2e290-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
