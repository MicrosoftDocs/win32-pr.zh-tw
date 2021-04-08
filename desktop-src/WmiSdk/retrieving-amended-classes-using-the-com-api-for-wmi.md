---
description: 如果您使用適用于 WMI 的 COM API 來取得或儲存當地語系化的類別資訊，請在 IWbemLocator：： ConnectServer 介面的 strLocale 參數中指定地區設定。
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: 使用適用于 WMI 的 COM API 來抓取修改過的類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0178b0b99de2b666e2f497074a02b02c49ba400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695148"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a><span data-ttu-id="7c64c-103">使用適用于 WMI 的 COM API 來抓取修改過的類別</span><span class="sxs-lookup"><span data-stu-id="7c64c-103">Retrieving Amended Classes Using the COM API for WMI</span></span>

<span data-ttu-id="7c64c-104">如果您使用適用于 WMI 的 COM API 來取得或儲存當地語系化的類別資訊，請在 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)介面的 *strLocale* 參數中指定地區設定。</span><span class="sxs-lookup"><span data-stu-id="7c64c-104">If you are using the COM API for WMI to retrieve or store localized class information, specify the locale in the *strLocale* parameter to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) interface.</span></span> <span data-ttu-id="7c64c-105">讀取或寫入修改過的類別時，表示您想要藉由指定 WBEM 旗標 \_ 使用 \_ \_ 修改過 \_ 的限定詞作為 *iFlags* 參數的旗標，以使用當地語系化的類別定義。</span><span class="sxs-lookup"><span data-stu-id="7c64c-105">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS as a flag for the *iFlags* parameter.</span></span>

<span data-ttu-id="7c64c-106">下表列出使用 WBEM 旗標之方法的同步和非同步版本， \_ \_ 請使用修改過的 \_ \_ 限定詞旗標。</span><span class="sxs-lookup"><span data-stu-id="7c64c-106">The following table lists the synchronous and asynchronous versions of the methods that use the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span>



| <span data-ttu-id="7c64c-107">同步方法</span><span class="sxs-lookup"><span data-stu-id="7c64c-107">Synchronous Method</span></span>                                                            | <span data-ttu-id="7c64c-108">非同步方法</span><span class="sxs-lookup"><span data-stu-id="7c64c-108">Asynchronous Method</span></span>                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c64c-109">**IWbemServices：： CreateClassEnum**</span><span class="sxs-lookup"><span data-stu-id="7c64c-109">**IWbemServices::CreateClassEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [<span data-ttu-id="7c64c-110">**IWbemServices：： CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="7c64c-110">**IWbemServices::CreateClassEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [<span data-ttu-id="7c64c-111">**IWbemServices：： CreateInstanceEnum**</span><span class="sxs-lookup"><span data-stu-id="7c64c-111">**IWbemServices::CreateInstanceEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [<span data-ttu-id="7c64c-112">**IWbemServices：： CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="7c64c-112">**IWbemServices::CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [<span data-ttu-id="7c64c-113">**IWbemServices：： ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="7c64c-113">**IWbemServices::ExecQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [<span data-ttu-id="7c64c-114">**IWbemServices：： ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="7c64c-114">**IWbemServices::ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [<span data-ttu-id="7c64c-115">**IWbemServices：： GetObject**</span><span class="sxs-lookup"><span data-stu-id="7c64c-115">**IWbemServices::GetObject**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [<span data-ttu-id="7c64c-116">**IWbemServices：： GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="7c64c-116">**IWbemServices::GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [<span data-ttu-id="7c64c-117">**IWbemServices：:P utClass**</span><span class="sxs-lookup"><span data-stu-id="7c64c-117">**IWbemServices::PutClass**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [<span data-ttu-id="7c64c-118">**IWbemServices：:P utClassAsync**</span><span class="sxs-lookup"><span data-stu-id="7c64c-118">**IWbemServices::PutClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [<span data-ttu-id="7c64c-119">**IWbemServices：:P utInstance**</span><span class="sxs-lookup"><span data-stu-id="7c64c-119">**IWbemServices::PutInstance**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [<span data-ttu-id="7c64c-120">**IWbemServices：:P utInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="7c64c-120">**IWbemServices::PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



