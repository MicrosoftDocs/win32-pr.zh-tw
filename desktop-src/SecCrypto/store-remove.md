---
description: Remove 方法會從開啟的憑證存放區移除憑證。 這個方法只能搭配以讀取/寫入權限開啟的存放區使用。
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Store. Remove 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 188553d6091314e1a872145219ea321d581b35c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976036"
---
# <a name="storeremove-method"></a><span data-ttu-id="35eda-104">Store. Remove 方法</span><span class="sxs-lookup"><span data-stu-id="35eda-104">Store.Remove method</span></span>

<span data-ttu-id="35eda-105">\[**Remove** 方法可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="35eda-105">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="35eda-106">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="35eda-106">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="35eda-107">**Remove** 方法會從開啟的 [*憑證存放區*](../secgloss/c-gly.md)移除 [*憑證*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="35eda-107">The **Remove** method removes a [*certificate*](../secgloss/c-gly.md) from an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="35eda-108">這個方法只能搭配以讀取/寫入權限開啟的存放區使用。</span><span class="sxs-lookup"><span data-stu-id="35eda-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="35eda-109">語法</span><span class="sxs-lookup"><span data-stu-id="35eda-109">Syntax</span></span>


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="35eda-110">參數</span><span class="sxs-lookup"><span data-stu-id="35eda-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35eda-111">*憑證* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35eda-111">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35eda-112">解析為要從存放區移除的 [**憑證**](certificate.md) 物件實例的運算式。</span><span class="sxs-lookup"><span data-stu-id="35eda-112">Expression that resolves to an instance of a [**Certificate**](certificate.md) object to be removed from the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35eda-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="35eda-113">Return value</span></span>

<span data-ttu-id="35eda-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="35eda-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35eda-115">備註</span><span class="sxs-lookup"><span data-stu-id="35eda-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35eda-116">從 web 腳本呼叫這個方法時，腳本必須刪除本機電腦上的數位憑證。</span><span class="sxs-lookup"><span data-stu-id="35eda-116">When this method is called from a web script, the script needs to delete digital certificates from the local computer.</span></span> <span data-ttu-id="35eda-117">允許不受信任的網站刪除數位憑證有安全性風險。</span><span class="sxs-lookup"><span data-stu-id="35eda-117">Allowing untrusted websites to delete digital certificates is a security risk.</span></span> <span data-ttu-id="35eda-118">此對話方塊會詢問第一次呼叫此方法時，網站是否可以刪除憑證。</span><span class="sxs-lookup"><span data-stu-id="35eda-118">A dialog box that asks whether the website can delete certificates appears when this method is first called.</span></span> <span data-ttu-id="35eda-119">如果您允許應用程式刪除憑證，然後選取 [不要再顯示此對話方塊]，則在該網域內刪除憑證的所有腳本都不會再出現此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="35eda-119">If you allow the application to delete certificates and select "Do not show this dialog box again," the dialog box will no longer appear for any script that deletes certificates within that domain.</span></span> <span data-ttu-id="35eda-120">不過，嘗試刪除憑證的網域以外的腳本仍會出現此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="35eda-120">However, scripts outside that domain that attempt to delete certificates will still cause this dialog box to appear.</span></span> <span data-ttu-id="35eda-121">如果您不允許腳本刪除憑證，然後選取 [不要再顯示此對話方塊]，則該網域內的腳本將會自動拒絕刪除憑證的能力。</span><span class="sxs-lookup"><span data-stu-id="35eda-121">If you do not allow the script to delete certificates and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to delete certificates.</span></span>

 

<span data-ttu-id="35eda-122">當您從存放區刪除憑證時，您應該先刪除與憑證相關聯的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="35eda-122">When you delete a certificate from a store, you should first delete the private key associated with the certificate.</span></span>

<span data-ttu-id="35eda-123">如果存放區未以讀取/寫入權限開啟，這個方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="35eda-123">If the store is not open with read/write permission, this method fails.</span></span> <span data-ttu-id="35eda-124">雖然這個方法可以與記憶體存放區搭配使用，但是在關閉存放區時，不會保存對記憶體存放區所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="35eda-124">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="35eda-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="35eda-125">Requirements</span></span>



| <span data-ttu-id="35eda-126">需求</span><span class="sxs-lookup"><span data-stu-id="35eda-126">Requirement</span></span> | <span data-ttu-id="35eda-127">值</span><span class="sxs-lookup"><span data-stu-id="35eda-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35eda-128">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="35eda-128">Redistributable</span></span><br/> | <span data-ttu-id="35eda-129">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="35eda-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="35eda-130">DLL</span><span class="sxs-lookup"><span data-stu-id="35eda-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="35eda-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35eda-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35eda-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35eda-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35eda-133">**市集**</span><span class="sxs-lookup"><span data-stu-id="35eda-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="35eda-134">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="35eda-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
