---
description: 表示建立 FhConfigMgr 物件時所使用之使用者的檔案歷程記錄設定。 所有設定作業都是藉由呼叫 IFhConfigMgr 介面的方法來執行。
ms.assetid: CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788
title: 'FhConfigMgr 類別 (Fhcfg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhConfigMgr
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 083ce344e44035b5872d91ad14465659defc8229
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847270"
---
# <a name="fhconfigmgr-class"></a><span data-ttu-id="c76ec-104">FhConfigMgr 類別</span><span class="sxs-lookup"><span data-stu-id="c76ec-104">FhConfigMgr class</span></span>

<span data-ttu-id="c76ec-105">表示建立 **FhConfigMgr** 物件時所使用之使用者的檔案歷程記錄設定。</span><span class="sxs-lookup"><span data-stu-id="c76ec-105">Represents the File History configuration of the user under which the **FhConfigMgr** object is created.</span></span> <span data-ttu-id="c76ec-106">所有設定作業都是藉由呼叫 [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) 介面的方法來執行。</span><span class="sxs-lookup"><span data-stu-id="c76ec-106">All configuration operations are performed by calling the methods of the [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="c76ec-107">執行時機</span><span class="sxs-lookup"><span data-stu-id="c76ec-107">When to implement</span></span>

<span data-ttu-id="c76ec-108">檔案歷程記錄 API 會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="c76ec-108">The File History API implements this class.</span></span> <span data-ttu-id="c76ec-109">若要建立這個類別的實例，請使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數。</span><span class="sxs-lookup"><span data-stu-id="c76ec-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c76ec-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="c76ec-110">Requirements</span></span>



| <span data-ttu-id="c76ec-111">需求</span><span class="sxs-lookup"><span data-stu-id="c76ec-111">Requirement</span></span> | <span data-ttu-id="c76ec-112">值</span><span class="sxs-lookup"><span data-stu-id="c76ec-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c76ec-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c76ec-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c76ec-114">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c76ec-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c76ec-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c76ec-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c76ec-116">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c76ec-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c76ec-117">標頭</span><span class="sxs-lookup"><span data-stu-id="c76ec-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c76ec-118"><dt>Fhcfg。h</dt></span><span class="sxs-lookup"><span data-stu-id="c76ec-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="c76ec-119">Idl</span><span class="sxs-lookup"><span data-stu-id="c76ec-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c76ec-120"><dt>Fhcfg .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c76ec-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
