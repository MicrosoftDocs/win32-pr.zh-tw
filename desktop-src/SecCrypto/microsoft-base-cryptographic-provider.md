---
description: Microsoft 基礎密碼編譯提供者是 (CSP) 提供者的初始加密服務提供者，並與 CryptoAPI 版本1.0 和2.0 一起散發。 這是一般用途的提供者，可支援數位簽章和資料加密。
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Microsoft 基礎密碼編譯提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc48060305337dd878dedcadca8cfed52bd2f34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971242"
---
# <a name="microsoft-base-cryptographic-provider"></a><span data-ttu-id="418e4-104">Microsoft 基礎密碼編譯提供者</span><span class="sxs-lookup"><span data-stu-id="418e4-104">Microsoft Base Cryptographic Provider</span></span>

<span data-ttu-id="418e4-105">Microsoft 基礎密碼編譯提供者是 (CSP) 提供者的初始 [*加密服務提供*](../secgloss/c-gly.md) 商，並與 [*CryptoAPI*](../secgloss/c-gly.md) 版本1.0 和2.0 一起散發。</span><span class="sxs-lookup"><span data-stu-id="418e4-105">The Microsoft Base Cryptographic Provider is the initial [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) provider, and is distributed with [*CryptoAPI*](../secgloss/c-gly.md) versions 1.0 and 2.0.</span></span> <span data-ttu-id="418e4-106">這是一般用途的提供者，可支援 [*數位簽章*](../secgloss/d-gly.md) 和資料加密。</span><span class="sxs-lookup"><span data-stu-id="418e4-106">It is a general-purpose provider that supports [*digital signatures*](../secgloss/d-gly.md) and data encryption.</span></span>

<span data-ttu-id="418e4-107">RSA 公開金鑰演算法可用於所有的公開金鑰作業。</span><span class="sxs-lookup"><span data-stu-id="418e4-107">The RSA public key algorithm is used for all public key operations.</span></span>

<span data-ttu-id="418e4-108">為了維持與舊版的回溯相容性，新版的提供者會保留 Wincrypt 中名稱的1.0 指定。</span><span class="sxs-lookup"><span data-stu-id="418e4-108">To maintain backward compatibility with earlier versions the new version of the provider retains the version 1.0 designation of the name in Wincrypt.h.</span></span> <span data-ttu-id="418e4-109">不過，此提供者的2.0 版目前為出貨。</span><span class="sxs-lookup"><span data-stu-id="418e4-109">However, version 2.0 of this provider is currently shipping.</span></span> <span data-ttu-id="418e4-110">若要判斷使用中提供者的實際版本，請呼叫 [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) ，並將 *dwParam* 引數設定為 **PP \_ 版本**。</span><span class="sxs-lookup"><span data-stu-id="418e4-110">To determine the actual version of the provider in use, call [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with the *dwParam* argument set to **PP\_VERSION**.</span></span> <span data-ttu-id="418e4-111">如果在 *>pbdata* 中傳回0x0200，表示您的版本為2.0。</span><span class="sxs-lookup"><span data-stu-id="418e4-111">If 0x0200 is returned in *pbData*, then you have version 2.0.</span></span>

|                |                     |
|----------------|---------------------|
| <span data-ttu-id="418e4-112">提供者類型：</span><span class="sxs-lookup"><span data-stu-id="418e4-112">Provider type:</span></span> | <span data-ttu-id="418e4-113">**>PROV \_ RSA \_ FULL**</span><span class="sxs-lookup"><span data-stu-id="418e4-113">**PROV\_RSA\_FULL**</span></span> |
| <span data-ttu-id="418e4-114">提供者名稱：</span><span class="sxs-lookup"><span data-stu-id="418e4-114">Provider name:</span></span> | <span data-ttu-id="418e4-115">**MS \_ DEF \_ >PROV**</span><span class="sxs-lookup"><span data-stu-id="418e4-115">**MS\_DEF\_PROV**</span></span>   |



 

 

 
