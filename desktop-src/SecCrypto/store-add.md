---
description: 將憑證物件新增至開啟的憑證存放區。
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Store. Add 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d217c784fa5f994e88ee2de78f2e1944091d724
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996205"
---
# <a name="storeadd-method"></a><span data-ttu-id="22819-103">Store. Add 方法</span><span class="sxs-lookup"><span data-stu-id="22819-103">Store.Add method</span></span>

<span data-ttu-id="22819-104">\[**Add** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="22819-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="22819-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/previous-versions/windows/embedded/hh424027(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="22819-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="22819-106">**Add** 方法會將 [**憑證**](certificate.md)物件新增至開啟的 [*憑證存放區*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="22819-106">The **Add** method adds a [**Certificate**](certificate.md) object to an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="22819-107">這個方法只能搭配以讀取/寫入權限開啟的存放區使用。</span><span class="sxs-lookup"><span data-stu-id="22819-107">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="22819-108">語法</span><span class="sxs-lookup"><span data-stu-id="22819-108">Syntax</span></span>


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="22819-109">參數</span><span class="sxs-lookup"><span data-stu-id="22819-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22819-110">*憑證* \[在\]</span><span class="sxs-lookup"><span data-stu-id="22819-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22819-111">解析為要加入至存放區之 [**憑證**](certificate.md) 物件的運算式。</span><span class="sxs-lookup"><span data-stu-id="22819-111">Expression that resolves to a [**Certificate**](certificate.md) object to be added to the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22819-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="22819-112">Return value</span></span>

<span data-ttu-id="22819-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="22819-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22819-114">備註</span><span class="sxs-lookup"><span data-stu-id="22819-114">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22819-115">從 web 腳本在系統存放區上呼叫這個方法時，腳本必須存取本機電腦上的數位憑證。</span><span class="sxs-lookup"><span data-stu-id="22819-115">When this method is called on a system store from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="22819-116">如果您允許腳本存取您的數位憑證，執行腳本的網站也可以存取儲存在憑證中的任何個人資訊。</span><span class="sxs-lookup"><span data-stu-id="22819-116">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="22819-117">第一次從特定網域呼叫這個方法時，會產生一個對話方塊，使用者必須在此對話方塊中指出是否允許存取憑證。</span><span class="sxs-lookup"><span data-stu-id="22819-117">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="22819-118">如果存放區未在讀取/寫入模式中開啟，則此方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="22819-118">If the store is not open in read/write mode, this method fails.</span></span> <span data-ttu-id="22819-119">雖然這個方法可以與記憶體存放區搭配使用，但是在關閉存放區時，不會保存對記憶體存放區所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="22819-119">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

<span data-ttu-id="22819-120">如果要新增至存放區的憑證與已存在的憑證相同，則 **Add** 方法會從存放區刪除現有的憑證，然後新增憑證。</span><span class="sxs-lookup"><span data-stu-id="22819-120">If the certificate being added to the store is the same as one that is already there, the **Add** method deletes the existing certificate from the store and then adds the new certificate.</span></span> <span data-ttu-id="22819-121">新的憑證會繼承現有憑證的屬性。</span><span class="sxs-lookup"><span data-stu-id="22819-121">The new certificate inherits properties from the existing certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="22819-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="22819-122">Requirements</span></span>



| <span data-ttu-id="22819-123">需求</span><span class="sxs-lookup"><span data-stu-id="22819-123">Requirement</span></span> | <span data-ttu-id="22819-124">值</span><span class="sxs-lookup"><span data-stu-id="22819-124">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22819-125">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="22819-125">Redistributable</span></span><br/> | <span data-ttu-id="22819-126">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="22819-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="22819-127">DLL</span><span class="sxs-lookup"><span data-stu-id="22819-127">DLL</span></span><br/>             | <dl> <span data-ttu-id="22819-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22819-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22819-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22819-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22819-130">**市集**</span><span class="sxs-lookup"><span data-stu-id="22819-130">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="22819-131">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="22819-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
