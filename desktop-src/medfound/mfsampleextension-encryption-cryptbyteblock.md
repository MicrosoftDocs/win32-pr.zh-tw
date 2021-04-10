---
description: 指定以範例為基礎的模式加密的加密位元組區塊大小。
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: 'MFSampleExtension_Encryption_CryptByteBlock 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026534"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a><span data-ttu-id="db53c-103">MFSampleExtension \_ Encryption \_ CryptByteBlock 屬性</span><span class="sxs-lookup"><span data-stu-id="db53c-103">MFSampleExtension\_Encryption\_CryptByteBlock attribute</span></span>

<span data-ttu-id="db53c-104">指定以範例為基礎的模式加密的加密位元組區塊大小。</span><span class="sxs-lookup"><span data-stu-id="db53c-104">Specifies the encrypted byte block size for sample-based pattern encryption.</span></span>

## <a name="data-type"></a><span data-ttu-id="db53c-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="db53c-105">Data type</span></span>

<span data-ttu-id="db53c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="db53c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="db53c-107">備註</span><span class="sxs-lookup"><span data-stu-id="db53c-107">Remarks</span></span>

<span data-ttu-id="db53c-108">Subsample 對應區塊中的 clear (非加密) 位元組數目是在 [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) 屬性中指定。</span><span class="sxs-lookup"><span data-stu-id="db53c-108">The number of clear (non-encrypted) bytes in the subsample mapping block are specified in the [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) attribute.</span></span> <span data-ttu-id="db53c-109">如果其中一個屬性不存在或值為0，則表示範例資料不會加密。</span><span class="sxs-lookup"><span data-stu-id="db53c-109">If either of these attributes are not present or have a value of 0, it means that the sample data is not encrypted.</span></span> <span data-ttu-id="db53c-110">這兩個值都必須為非零、正值或兩者都必須有零值。</span><span class="sxs-lookup"><span data-stu-id="db53c-110">Either both of these values must be non-zero, positive values, or both must have a value of zero.</span></span>

<span data-ttu-id="db53c-111">如果來源是以值為基礎，則會根據 [ \_ crypt] \_ ( [tenc] ) 在 [配置] 標頭中的 [預設值] 位元組區塊的值來設定值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="db53c-111">In cases where the Source is MP4-based, the value is set based off the values of default\_crypt\_byte\_block within the track encryption box (‘tenc’) in the MP4 header.</span></span> <span data-ttu-id="db53c-112">如需詳細資訊，請參閱 [MFSampleExtension \_ 加密 \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md)。</span><span class="sxs-lookup"><span data-stu-id="db53c-112">For more information, see [MFSampleExtension\_Encryption\_ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db53c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="db53c-113">Requirements</span></span>



| <span data-ttu-id="db53c-114">需求</span><span class="sxs-lookup"><span data-stu-id="db53c-114">Requirement</span></span> | <span data-ttu-id="db53c-115">值</span><span class="sxs-lookup"><span data-stu-id="db53c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db53c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db53c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="db53c-117">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db53c-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="db53c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db53c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="db53c-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="db53c-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="db53c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="db53c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="db53c-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="db53c-121"><dt>Mfidl.h</dt></span></span> </dl> |



 

 




