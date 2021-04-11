---
title: IMsRdpClientNonScriptable5 RemoteMonitorLayoutMatchesLocal 屬性
description: 指定遠端監視配置是否與本機監視器版面配置相同。
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- RemoteMonitorLayoutMatchesLocal 屬性遠端桌面服務
- RemoteMonitorLayoutMatchesLocal 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，RemoteMonitorLayoutMatchesLocal 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5018b22865cc683fc9231c857a1b99b8acbfeca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104621"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a><span data-ttu-id="39b1b-106">IMsRdpClientNonScriptable5：： RemoteMonitorLayoutMatchesLocal 屬性</span><span class="sxs-lookup"><span data-stu-id="39b1b-106">IMsRdpClientNonScriptable5::RemoteMonitorLayoutMatchesLocal property</span></span>

<span data-ttu-id="39b1b-107">指定遠端監視配置是否與本機監視器版面配置相同。</span><span class="sxs-lookup"><span data-stu-id="39b1b-107">Specifies if the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="39b1b-108">如果此屬性包含 **VARIANT \_ TRUE**，則遠端監視配置與本機監視器版面配置相同。</span><span class="sxs-lookup"><span data-stu-id="39b1b-108">If this property contains **VARIANT\_TRUE**, the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="39b1b-109">如果此屬性包含 **變體 \_ FALSE**，則遠端和本機監視器會有不同的版面配置。</span><span class="sxs-lookup"><span data-stu-id="39b1b-109">If this property contains **VARIANT\_FALSE**, the remote and local monitors have different layouts.</span></span>

<span data-ttu-id="39b1b-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="39b1b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b1b-111">語法</span><span class="sxs-lookup"><span data-stu-id="39b1b-111">Syntax</span></span>


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a><span data-ttu-id="39b1b-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="39b1b-112">Property value</span></span>

<span data-ttu-id="39b1b-113">接收屬性值。</span><span class="sxs-lookup"><span data-stu-id="39b1b-113">Receives the property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b1b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="39b1b-114">Requirements</span></span>



| <span data-ttu-id="39b1b-115">需求</span><span class="sxs-lookup"><span data-stu-id="39b1b-115">Requirement</span></span> | <span data-ttu-id="39b1b-116">值</span><span class="sxs-lookup"><span data-stu-id="39b1b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39b1b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39b1b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="39b1b-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39b1b-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39b1b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39b1b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="39b1b-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39b1b-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="39b1b-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="39b1b-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="39b1b-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39b1b-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="39b1b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="39b1b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39b1b-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39b1b-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="39b1b-125">IID</span><span class="sxs-lookup"><span data-stu-id="39b1b-125">IID</span></span><br/>                      | <span data-ttu-id="39b1b-126">IID \_ IMsRdpClientNonScriptable5 定義為 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="39b1b-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39b1b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39b1b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b1b-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="39b1b-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





