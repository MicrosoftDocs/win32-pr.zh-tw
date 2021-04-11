---
description: 可以在 IMFOutputPolicy 上設定的識別碼。
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: MF_POLICY_ID (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787195b20980164d7534bccc267781cdbb7510e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027466"
---
# <a name="mf_policy_id-attribute"></a><span data-ttu-id="bd0c2-103">MF \_ 原則 \_ 識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="bd0c2-103">MF\_POLICY\_ID attribute</span></span>

<span data-ttu-id="bd0c2-104">可以在 [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)上設定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd0c2-104">An identifier that can be set on an [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy).</span></span>

## <a name="data-type"></a><span data-ttu-id="bd0c2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="bd0c2-105">Data type</span></span>

<span data-ttu-id="bd0c2-106">**UINT32** (視為 **BOOL**) </span><span class="sxs-lookup"><span data-stu-id="bd0c2-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="remarks"></a><span data-ttu-id="bd0c2-107">備註</span><span class="sxs-lookup"><span data-stu-id="bd0c2-107">Remarks</span></span>

<span data-ttu-id="bd0c2-108">您可以從 [MEPolicySet](./mepolicyset.md) 媒體事件接收值。</span><span class="sxs-lookup"><span data-stu-id="bd0c2-108">The value can be recieved from the [MEPolicySet](./mepolicyset.md) media event.</span></span> <span data-ttu-id="bd0c2-109">它會儲存為 **MEPolicySet** 事件中的 **VT_UI4** 型別承載。</span><span class="sxs-lookup"><span data-stu-id="bd0c2-109">It is stored as a **VT_UI4** type payload in the **MEPolicySet** event.</span></span>


## <a name="requirements"></a><span data-ttu-id="bd0c2-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd0c2-110">Requirements</span></span>



| <span data-ttu-id="bd0c2-111">需求</span><span class="sxs-lookup"><span data-stu-id="bd0c2-111">Requirement</span></span> | <span data-ttu-id="bd0c2-112">值</span><span class="sxs-lookup"><span data-stu-id="bd0c2-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bd0c2-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd0c2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="bd0c2-114">Windows 10 2020 年4月更新</span><span class="sxs-lookup"><span data-stu-id="bd0c2-114">Windows 10 April 2020 Update</span></span>   <br/>                                      |
| <span data-ttu-id="bd0c2-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd0c2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="bd0c2-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd0c2-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bd0c2-117">標頭</span><span class="sxs-lookup"><span data-stu-id="bd0c2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd0c2-118"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd0c2-118"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd0c2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd0c2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd0c2-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="bd0c2-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>



 

 
