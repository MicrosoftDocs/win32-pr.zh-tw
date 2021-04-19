---
description: 定義方法的輸入和輸出參數。
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: __PARAMETERS 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980898"
---
# <a name="__parameters-class"></a><span data-ttu-id="46dc9-103">\_\_PARAMETERS 類別</span><span class="sxs-lookup"><span data-stu-id="46dc9-103">\_\_PARAMETERS class</span></span>

<span data-ttu-id="46dc9-104">**\_ \_ 參數** 系統類別是定義方法之輸入和輸出參數的抽象類別。</span><span class="sxs-lookup"><span data-stu-id="46dc9-104">The **\_\_PARAMETERS** system class is an abstract class that defines the input and output parameters for methods.</span></span> <span data-ttu-id="46dc9-105">它也可用來傳遞 WMI 用戶端與方法提供者之間的輸入和輸出參數值。</span><span class="sxs-lookup"><span data-stu-id="46dc9-105">It is also used to pass input and output parameter values between a WMI client and a method provider.</span></span>

<span data-ttu-id="46dc9-106">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="46dc9-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="46dc9-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="46dc9-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="46dc9-108">語法</span><span class="sxs-lookup"><span data-stu-id="46dc9-108">Syntax</span></span>

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a><span data-ttu-id="46dc9-109">成員</span><span class="sxs-lookup"><span data-stu-id="46dc9-109">Members</span></span>

<span data-ttu-id="46dc9-110">**\_ \_ PARAMETERS** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="46dc9-110">The **\_\_PARAMETERS** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="46dc9-111">備註</span><span class="sxs-lookup"><span data-stu-id="46dc9-111">Remarks</span></span>

<span data-ttu-id="46dc9-112">若要定義使用者類別中的方法，WMI 用戶端會建立 **\_ \_ PARAMETERS** 類別的複本，並為方法中的每個輸入參數加入屬性。</span><span class="sxs-lookup"><span data-stu-id="46dc9-112">To define a method in a user class, a WMI client creates a copy of the **\_\_PARAMETERS** class, and adds a property for each input parameter in a method.</span></span> <span data-ttu-id="46dc9-113">如果方法包含傳回值或輸出參數，則必須建立 **\_ \_ 參數** 的另一個複本。</span><span class="sxs-lookup"><span data-stu-id="46dc9-113">If the method contains a return value or output parameters, another copy of **\_\_PARAMETERS** must be created.</span></span> <span data-ttu-id="46dc9-114">如果方法傳回傳回值，則用戶端必須加入名為 **ReturnValue** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="46dc9-114">If the method returns a return value, the client must add a property named **ReturnValue**.</span></span> <span data-ttu-id="46dc9-115">然後，方法提供者會使用 [**IWbemClassObject：:P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)的呼叫來儲存方法參數。</span><span class="sxs-lookup"><span data-stu-id="46dc9-115">The method provider then stores the method parameters with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="46dc9-116">若要叫用方法，用戶端會依序呼叫下列各項：</span><span class="sxs-lookup"><span data-stu-id="46dc9-116">To invoke a method, a client calls the following in sequence:</span></span>

1.  <span data-ttu-id="46dc9-117">[**IWbemClassObject：： GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) ，以抓取 [**IWbemClassObject：:P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)儲存的 **\_ \_ PARAMETERS** 類別的複本。</span><span class="sxs-lookup"><span data-stu-id="46dc9-117">[**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve a copy of the **\_\_PARAMETERS** class that is stored by [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>
2.  <span data-ttu-id="46dc9-118">[**IWbemClassObject：： SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)，然後為方法的每個輸入參數設定一個屬性。</span><span class="sxs-lookup"><span data-stu-id="46dc9-118">[**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), and then sets one property for each input parameter to the method.</span></span>
3.  <span data-ttu-id="46dc9-119">[**Iwbemservices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) 或 [**Iwbemservices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) ，以執行方法。</span><span class="sxs-lookup"><span data-stu-id="46dc9-119">[**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) to execute the method.</span></span>

<span data-ttu-id="46dc9-120">在方法完成執行之後，如果方法有輸出參數或傳回值，則可能會傳回另一個 **\_ \_ 參數** 類別實例。</span><span class="sxs-lookup"><span data-stu-id="46dc9-120">After the method is finished executing, another **\_\_PARAMETERS** class instance may be returned if the method has output parameters or a return value.</span></span>

-   <span data-ttu-id="46dc9-121">如果使用 [**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)叫用方法，則 **\_ \_ 參數** 實例會以 output 引數傳回。</span><span class="sxs-lookup"><span data-stu-id="46dc9-121">If the method was invoked by using [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), the **\_\_PARAMETERS** instance is returned as an output argument.</span></span>
-   <span data-ttu-id="46dc9-122">如果使用 [**IWbemServices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)叫用方法，則 **\_ \_ 參數** 實例會以參數形式傳回給 [**IWbemObjectSink：：表示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)。</span><span class="sxs-lookup"><span data-stu-id="46dc9-122">If the method was invoked by using [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), the **\_\_PARAMETERS** instance is returned as a parameter to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span>

## <a name="requirements"></a><span data-ttu-id="46dc9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="46dc9-123">Requirements</span></span>



| <span data-ttu-id="46dc9-124">需求</span><span class="sxs-lookup"><span data-stu-id="46dc9-124">Requirement</span></span> | <span data-ttu-id="46dc9-125">值</span><span class="sxs-lookup"><span data-stu-id="46dc9-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="46dc9-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46dc9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="46dc9-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46dc9-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="46dc9-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46dc9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="46dc9-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46dc9-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="46dc9-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="46dc9-130">Namespace</span></span><br/>                | <span data-ttu-id="46dc9-131">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="46dc9-131">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="46dc9-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46dc9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46dc9-133">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="46dc9-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="46dc9-134">**IWbemServices：： ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="46dc9-134">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="46dc9-135">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="46dc9-135">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 




