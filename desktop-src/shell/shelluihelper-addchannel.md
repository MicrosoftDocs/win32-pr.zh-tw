---
description: 將新通道新增至 Windows Internet Explorer [我的最愛] 功能表中的通道清單和桌面上的 [頻道] 列。
title: 'ShellUIHelper. AddChannel 方法 (Exdisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: d08c1360cb2a96fbc7b87daecb650bbf46aa6ad9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841199"
---
# <a name="shelluihelperaddchannel-method"></a><span data-ttu-id="6c6f8-103">ShellUIHelper. AddChannel 方法</span><span class="sxs-lookup"><span data-stu-id="6c6f8-103">ShellUIHelper.AddChannel method</span></span>

<span data-ttu-id="6c6f8-104">將新通道新增至 Windows Internet Explorer [我的最愛] 功能表中的通道清單和桌面上的 [**頻道** **]** 列。</span><span class="sxs-lookup"><span data-stu-id="6c6f8-104">Adds a new channel to the list of channels in the Windows Internet Explorer **Favorites** menu and to the **Channel** bar on the desktop.</span></span>

> [!Note]  
> <span data-ttu-id="6c6f8-105">Windows Vista 下已不再支援此方法。</span><span class="sxs-lookup"><span data-stu-id="6c6f8-105">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="6c6f8-106">在該作業系統下，它會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="6c6f8-106">Under that operating system, it returns E\_NOTIMPL.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6c6f8-107">語法</span><span class="sxs-lookup"><span data-stu-id="6c6f8-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="6c6f8-108">參數</span><span class="sxs-lookup"><span data-stu-id="6c6f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6f8-109">*sURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c6f8-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6f8-110">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6c6f8-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6c6f8-111">指定 CDF 檔案 URL 的 **字串** 值。</span><span class="sxs-lookup"><span data-stu-id="6c6f8-111">A **String** value that specifies the URL of the CDF file.</span></span>

> [!Note]  
> <span data-ttu-id="6c6f8-112">CDF 檔案中的連結必須使用 HTTP、HTTPS 或 FTP 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6c6f8-112">The links in the CDF file must use HTTP, HTTPS, or FTP protocols.</span></span> <span data-ttu-id="6c6f8-113">如果 CDF 檔案包含任何其他通訊協定，則通道的新增會失敗，而且不會顯示任何對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6c6f8-113">If the CDF file contains any other protocol, the addition of the channel fails and no dialog box appears.</span></span>

 

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="6c6f8-114">範例</span><span class="sxs-lookup"><span data-stu-id="6c6f8-114">Examples</span></span>

<span data-ttu-id="6c6f8-115">下列範例會針對內嵌于 HTML 和 Visual Basic 中的 JScript，顯示此方法的適當用法。</span><span class="sxs-lookup"><span data-stu-id="6c6f8-115">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="6c6f8-116">Jscript：</span><span class="sxs-lookup"><span data-stu-id="6c6f8-116">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



<span data-ttu-id="6c6f8-117">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="6c6f8-117">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6c6f8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c6f8-118">Requirements</span></span>



| <span data-ttu-id="6c6f8-119">需求</span><span class="sxs-lookup"><span data-stu-id="6c6f8-119">Requirement</span></span> | <span data-ttu-id="6c6f8-120">值</span><span class="sxs-lookup"><span data-stu-id="6c6f8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6f8-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c6f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6c6f8-122">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c6f8-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6c6f8-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c6f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6c6f8-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c6f8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6c6f8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6c6f8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c6f8-126"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c6f8-126"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="6c6f8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6c6f8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c6f8-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="6c6f8-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
