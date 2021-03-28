---
description: 將指定之 ShellFolderView 物件的事件轉送至對應的 ShellFolderViewOC 事件處理常式。
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: 'ShellFolderViewOC. SetFolderView 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973584"
---
# <a name="shellfolderviewocsetfolderview-method"></a><span data-ttu-id="527d3-103">ShellFolderViewOC. SetFolderView 方法</span><span class="sxs-lookup"><span data-stu-id="527d3-103">ShellFolderViewOC.SetFolderView method</span></span>

<span data-ttu-id="527d3-104">將指定之 [**ShellFolderView**](shellfolderview.md) 物件的事件轉送至對應的 [**ShellFolderViewOC**](shellfolderviewoc-object.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="527d3-104">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="527d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="527d3-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a><span data-ttu-id="527d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="527d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="527d3-107">*oShellFolderView* \[在\]</span><span class="sxs-lookup"><span data-stu-id="527d3-107">*oShellFolderView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="527d3-108">類型： \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _</span><span class="sxs-lookup"><span data-stu-id="527d3-108">Type: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\** _</span></span>

<span data-ttu-id="527d3-109">[_ *ShellFolderView* \*](shellfolderview.md)物件。</span><span class="sxs-lookup"><span data-stu-id="527d3-109">A [_ *ShellFolderView*\*](shellfolderview.md) object.</span></span> <span data-ttu-id="527d3-110">它的 [**EnumDone**](shellfolderviewoc-enumdone.md) 和 [**SelectionChanged**](shellfolderview-selectionchanged.md) 事件將會轉送到對應的 [**ShellFolderViewOC**](shellfolderviewoc-object.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="527d3-110">Its [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderview-selectionchanged.md) events will be forwarded to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="527d3-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="527d3-111">Requirements</span></span>



| <span data-ttu-id="527d3-112">需求</span><span class="sxs-lookup"><span data-stu-id="527d3-112">Requirement</span></span> | <span data-ttu-id="527d3-113">值</span><span class="sxs-lookup"><span data-stu-id="527d3-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="527d3-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="527d3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="527d3-115">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="527d3-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="527d3-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="527d3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="527d3-117">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="527d3-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="527d3-118">標頭</span><span class="sxs-lookup"><span data-stu-id="527d3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="527d3-119"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="527d3-119"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="527d3-120">Idl</span><span class="sxs-lookup"><span data-stu-id="527d3-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="527d3-121"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="527d3-121"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="527d3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="527d3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="527d3-123"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="527d3-123"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
