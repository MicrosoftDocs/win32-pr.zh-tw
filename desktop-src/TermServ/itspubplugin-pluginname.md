---
title: ItsPubPlugin pluginName 屬性
description: 捕獲外掛程式的名稱。
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- pluginName 屬性遠端桌面服務
- pluginName 屬性遠端桌面服務，ItsPubPlugin 介面
- ItsPubPlugin 介面遠端桌面服務，pluginName 屬性
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f5aa6ff6659047e9be48fd7b7a41f652c5cfd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968773"
---
# <a name="itspubpluginpluginname-property"></a><span data-ttu-id="52909-106">ItsPubPlugin：:p luginName 屬性</span><span class="sxs-lookup"><span data-stu-id="52909-106">ItsPubPlugin::pluginName property</span></span>

<span data-ttu-id="52909-107">捕獲外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="52909-107">Retrieves the name of the plug-in.</span></span>

<span data-ttu-id="52909-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="52909-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52909-109">語法</span><span class="sxs-lookup"><span data-stu-id="52909-109">Syntax</span></span>


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="52909-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="52909-110">Property value</span></span>

<span data-ttu-id="52909-111">**BSTR** 變數的指標，用來接收外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="52909-111">A pointer to a **BSTR** variable to receive the name of the plug-in.</span></span>

## <a name="requirements"></a><span data-ttu-id="52909-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="52909-112">Requirements</span></span>



| <span data-ttu-id="52909-113">需求</span><span class="sxs-lookup"><span data-stu-id="52909-113">Requirement</span></span> | <span data-ttu-id="52909-114">值</span><span class="sxs-lookup"><span data-stu-id="52909-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="52909-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52909-115">Minimum supported client</span></span><br/> | <span data-ttu-id="52909-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="52909-116">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="52909-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52909-117">Minimum supported server</span></span><br/> | <span data-ttu-id="52909-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="52909-118">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="52909-119">Idl</span><span class="sxs-lookup"><span data-stu-id="52909-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="52909-120"><dt>Cpubplugin .idl</dt></span><span class="sxs-lookup"><span data-stu-id="52909-120"><dt>Cpubplugin.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52909-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52909-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52909-122">**ItsPubPlugin**</span><span class="sxs-lookup"><span data-stu-id="52909-122">**ItsPubPlugin**</span></span>](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





