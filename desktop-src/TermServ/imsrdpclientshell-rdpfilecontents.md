---
title: IMsRdpClientShell RdpFileContents 屬性
description: 指定或抓取從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動的遠端桌面通訊協定 (RDP) 檔案內容。
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- RdpFileContents 屬性遠端桌面服務
- RdpFileContents 屬性遠端桌面服務，IMsRdpClientShell 介面
- IMsRdpClientShell 介面遠端桌面服務，RdpFileContents 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967744"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a><span data-ttu-id="7963c-106">IMsRdpClientShell：： RdpFileContents 屬性</span><span class="sxs-lookup"><span data-stu-id="7963c-106">IMsRdpClientShell::RdpFileContents property</span></span>

<span data-ttu-id="7963c-107">指定或抓取從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動的遠端桌面通訊協定 (RDP) 檔案內容。</span><span class="sxs-lookup"><span data-stu-id="7963c-107">Specifies or retrieves the Remote Desktop Protocol (RDP) file content to be launched from Remote Desktop Web Access (RD Web Access) or from some other web portal.</span></span>

<span data-ttu-id="7963c-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="7963c-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7963c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7963c-109">Syntax</span></span>


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a><span data-ttu-id="7963c-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="7963c-110">Property value</span></span>

<span data-ttu-id="7963c-111">指定要從 web 入口網站啟動的 RDP 檔案內容。</span><span class="sxs-lookup"><span data-stu-id="7963c-111">Specifies the RDP file content to be launched from the web portal.</span></span>

## <a name="requirements"></a><span data-ttu-id="7963c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7963c-112">Requirements</span></span>



| <span data-ttu-id="7963c-113">需求</span><span class="sxs-lookup"><span data-stu-id="7963c-113">Requirement</span></span> | <span data-ttu-id="7963c-114">值</span><span class="sxs-lookup"><span data-stu-id="7963c-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7963c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7963c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7963c-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7963c-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7963c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7963c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7963c-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7963c-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7963c-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7963c-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="7963c-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7963c-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7963c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7963c-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7963c-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7963c-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7963c-123">IID</span><span class="sxs-lookup"><span data-stu-id="7963c-123">IID</span></span><br/>                      | <span data-ttu-id="7963c-124">IID \_ IMsRdpClientShell 定義為 d012ae6d-c19a-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="7963c-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="7963c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7963c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7963c-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="7963c-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





