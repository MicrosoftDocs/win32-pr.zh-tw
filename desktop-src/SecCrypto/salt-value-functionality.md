---
description: 基底提供者會以零值 salt 的11個位元組建立40位的對稱金鑰，如果指定了 CRYPT CREATE salt，則會建立11個位元組的非零 salt， \_ \_ 或沒有 salt 值。
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Salt 值功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8e3049c431cf909c1008acac26925cd1fa9e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318715"
---
# <a name="salt-value-functionality"></a><span data-ttu-id="ae539-103">Salt 值功能</span><span class="sxs-lookup"><span data-stu-id="ae539-103">Salt Value Functionality</span></span>

<span data-ttu-id="ae539-104">基底提供者會以零值 [*salt*](../secgloss/s-gly.md)的11個位元組建立40位的 [*對稱金鑰*](../secgloss/s-gly.md)，如果指定了 CRYPT CREATE salt，則會建立11個位元組的非零 salt， \_ \_ 或沒有 salt 值。</span><span class="sxs-lookup"><span data-stu-id="ae539-104">The Base Provider creates 40-bit [*symmetric keys*](../secgloss/s-gly.md) created with eleven bytes of zero-value [*salt*](../secgloss/s-gly.md), eleven bytes of nonzero salt if CRYPT\_CREATE\_SALT is specified, or no salt value.</span></span> <span data-ttu-id="ae539-105">不過，具有零值 salt 的40位對稱金鑰，不等於沒有 salt 的40位對稱金鑰。</span><span class="sxs-lookup"><span data-stu-id="ae539-105">A 40-bit symmetric key with zero-value salt, however, is not equivalent to a 40-bit symmetric key without salt.</span></span> <span data-ttu-id="ae539-106">基於互通性，您必須建立金鑰，而不需要 salt。</span><span class="sxs-lookup"><span data-stu-id="ae539-106">For interoperability, keys must be created without salt.</span></span> <span data-ttu-id="ae539-107">此問題的原因是預設條件只會與40位的索引鍵完全相符。</span><span class="sxs-lookup"><span data-stu-id="ae539-107">This problem results from a default condition that occurs only with keys of exactly 40 bits.</span></span> <span data-ttu-id="ae539-108">所有其他 [*金鑰長度*](../secgloss/k-gly.md) 預設不會配置 salt。</span><span class="sxs-lookup"><span data-stu-id="ae539-108">All other [*key lengths*](../secgloss/k-gly.md) do not have salt allocated by default.</span></span>

<span data-ttu-id="ae539-109">基底提供者和延伸提供者都可以使用 CRYPT \_ NO \_ SALT 旗標來指定為40位對稱金鑰配置 SALT 值。</span><span class="sxs-lookup"><span data-stu-id="ae539-109">Both the Base Providers and the Extended Provider can use the CRYPT\_NO\_SALT flag to specify that no salt value is allocated for a 40-bit symmetric key.</span></span> <span data-ttu-id="ae539-110">接受此旗標的函式為 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)、 [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)和 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)。</span><span class="sxs-lookup"><span data-stu-id="ae539-110">The functions that accept this flag are [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey), and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="ae539-111">根據預設，這些函式會繼續使用11位元組長的零值 salt，為40位對稱金鑰案例提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="ae539-111">By default, these functions provide backward compatibility for the 40-bit symmetric key case by continuing the use of the eleven-byte-long zero-value salt.</span></span>

 

 
