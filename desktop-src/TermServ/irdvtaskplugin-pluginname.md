---
title: 'IRDVTaskPlugin PluginName 屬性 (Tspubplugincom .h) '
description: 包含工作代理程式的顯示名稱。
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- PluginName 屬性遠端桌面服務
- PluginName 屬性遠端桌面服務，IRDVTaskPlugin 介面
- IRDVTaskPlugin 介面遠端桌面服務，PluginName 屬性
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686051"
---
# <a name="irdvtaskpluginpluginname-property"></a><span data-ttu-id="2aa31-106">IRDVTaskPlugin：:P luginName 屬性</span><span class="sxs-lookup"><span data-stu-id="2aa31-106">IRDVTaskPlugin::PluginName property</span></span>

<span data-ttu-id="2aa31-107">包含工作代理程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2aa31-107">Contains the display name of the task agent.</span></span> <span data-ttu-id="2aa31-108">此名稱僅供記錄之用。</span><span class="sxs-lookup"><span data-stu-id="2aa31-108">This name is used for logging purposes only.</span></span>

<span data-ttu-id="2aa31-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2aa31-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aa31-110">語法</span><span class="sxs-lookup"><span data-stu-id="2aa31-110">Syntax</span></span>


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="2aa31-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="2aa31-111">Property value</span></span>

<span data-ttu-id="2aa31-112">工作代理程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2aa31-112">The display name of the task agent.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aa31-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2aa31-113">Requirements</span></span>



| <span data-ttu-id="2aa31-114">需求</span><span class="sxs-lookup"><span data-stu-id="2aa31-114">Requirement</span></span> | <span data-ttu-id="2aa31-115">值</span><span class="sxs-lookup"><span data-stu-id="2aa31-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa31-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2aa31-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2aa31-117">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="2aa31-117">Windows 7 Enterprise</span></span><br/>                                                             |
| <span data-ttu-id="2aa31-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2aa31-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2aa31-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2aa31-119">Windows Server 2008 R2</span></span><br/>                                                           |
| <span data-ttu-id="2aa31-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2aa31-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2aa31-121"><dt>Tspubplugincom。h</dt></span><span class="sxs-lookup"><span data-stu-id="2aa31-121"><dt>Tspubplugincom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aa31-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2aa31-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aa31-123">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="2aa31-123">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





