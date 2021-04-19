---
description: 匯入方法會將先前匯出的憑證存放區內容複寫到開啟的憑證存放區。 這個方法只能搭配以讀取/寫入權限開啟的存放區使用。
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Store. Import 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999453"
---
# <a name="storeimport-method"></a><span data-ttu-id="7658e-104">Store. Import 方法</span><span class="sxs-lookup"><span data-stu-id="7658e-104">Store.Import method</span></span>

<span data-ttu-id="7658e-105">\[匯 **入** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="7658e-105">\[The **Import** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7658e-106">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/previous-versions/windows/embedded/hh424027(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="7658e-106">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7658e-107">匯 **入** 方法會將先前匯出的憑證存放區內容複寫到開啟的 [*憑證存放區*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="7658e-107">The **Import** method copies into an open [*certificate store*](../secgloss/c-gly.md) the contents of a previously exported certificate store.</span></span> <span data-ttu-id="7658e-108">這個方法只能搭配以讀取/寫入權限開啟的存放區使用。</span><span class="sxs-lookup"><span data-stu-id="7658e-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="7658e-109">語法</span><span class="sxs-lookup"><span data-stu-id="7658e-109">Syntax</span></span>


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a><span data-ttu-id="7658e-110">參數</span><span class="sxs-lookup"><span data-stu-id="7658e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7658e-111">*EncodedStore* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7658e-111">*EncodedStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7658e-112">包含要匯入之編碼憑證的字串。</span><span class="sxs-lookup"><span data-stu-id="7658e-112">The string that contains the encoded certificates to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7658e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7658e-113">Return value</span></span>

<span data-ttu-id="7658e-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7658e-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7658e-115">備註</span><span class="sxs-lookup"><span data-stu-id="7658e-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7658e-116">從 web 腳本呼叫這個方法時，腳本必須存取本機電腦上的數位憑證。</span><span class="sxs-lookup"><span data-stu-id="7658e-116">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="7658e-117">如果您允許腳本存取您的數位憑證，執行腳本的網站也可以存取儲存在憑證中的任何個人資訊。</span><span class="sxs-lookup"><span data-stu-id="7658e-117">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="7658e-118">第一次從特定網域呼叫這個方法時，會產生一個對話方塊，使用者必須在此對話方塊中指出是否允許存取憑證。</span><span class="sxs-lookup"><span data-stu-id="7658e-118">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="7658e-119">如果存放區未以讀取/寫入權限開啟，這個方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="7658e-119">If the store is not opened with read/write permission, this method fails.</span></span> <span data-ttu-id="7658e-120">雖然這個方法可以與記憶體存放區搭配使用，但是在關閉存放區時，不會保存對記憶體存放區所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="7658e-120">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7658e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7658e-121">Requirements</span></span>



| <span data-ttu-id="7658e-122">需求</span><span class="sxs-lookup"><span data-stu-id="7658e-122">Requirement</span></span> | <span data-ttu-id="7658e-123">值</span><span class="sxs-lookup"><span data-stu-id="7658e-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7658e-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7658e-124">Redistributable</span></span><br/> | <span data-ttu-id="7658e-125">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7658e-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7658e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7658e-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="7658e-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7658e-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7658e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7658e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7658e-129">**市集**</span><span class="sxs-lookup"><span data-stu-id="7658e-129">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="7658e-130">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="7658e-130">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
