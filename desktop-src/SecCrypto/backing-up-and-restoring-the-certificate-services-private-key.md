---
description: 您無法使用 Certadm.dll 的備份和還原功能來備份憑證服務私密金鑰。
ms.assetid: 27ee8caa-8f5e-46dc-b55d-afde5471507e
title: 備份和還原憑證服務私密金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 891794f36e87b2aa4b6a5d5c8dde55304da20601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974060"
---
# <a name="backing-up-and-restoring-the-certificate-services-private-key"></a><span data-ttu-id="c5c4d-103">備份和還原憑證服務私密金鑰</span><span class="sxs-lookup"><span data-stu-id="c5c4d-103">Backing Up and Restoring the Certificate Services Private Key</span></span>

<span data-ttu-id="c5c4d-104">您無法使用 Certadm.dll 的備份和還原功能來備份憑證服務 [*私密金鑰*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="c5c4d-104">You cannot use the Certadm.dll's backup and restore functions to back up the Certificate Services [*private keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="c5c4d-105">這些函式無法備份私密金鑰，因為這些函式的目的是要備份和還原憑證服務資料庫 (以及) 的相關檔案，而且此資料庫不包含任何 (的私密金鑰，即使是) 自我發行的憑證也一樣。</span><span class="sxs-lookup"><span data-stu-id="c5c4d-105">Private keys cannot be backed up by these functions because these functions are intended to backup and restore the Certificate Services database (and related files), and this database does not contain any private keys (even for self-issued certificates).</span></span>

<span data-ttu-id="c5c4d-106">若要備份憑證服務私密金鑰，請使用「憑證授權單位單位」 MMC 嵌入式管理單元，或使用 certutil 命令 (搭配-backup 或-backupkey 指定的) 。</span><span class="sxs-lookup"><span data-stu-id="c5c4d-106">To back up a Certificate Services private key, use the Certification Authority MMC snap-in, or the certutil command (with -backup or -backupkey specified).</span></span> <span data-ttu-id="c5c4d-107">使用「憑證授權單位單位」 MMC 嵌入式管理單元或 certutil 來備份私密金鑰會導致私密金鑰寫入 PKCS 12 檔案中 \# 。</span><span class="sxs-lookup"><span data-stu-id="c5c4d-107">Backing up the private key with the Certification Authority MMC snap-in or certutil results in the private key being written to PKCS \#12 file.</span></span> <span data-ttu-id="c5c4d-108">雖然這個 PKCS \# 12 檔案受密碼保護，但它應該被視為非常機密，而且必須安全地儲存; PKCS 12 檔案的密碼 \# 也應受未經授權的人員保護。</span><span class="sxs-lookup"><span data-stu-id="c5c4d-108">Even though this PKCS \#12 file is password-protected, it should be considered extremely sensitive and must be stored securely; the password to the PKCS \#12 file should also be guarded from unauthorized persons.</span></span>

<span data-ttu-id="c5c4d-109">同樣地，憑證服務的備份和還原功能無法還原私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5c4d-109">Similarly, private keys cannot be restored by the Certificate Services backup and restore functions.</span></span> <span data-ttu-id="c5c4d-110">PKCS 12 檔案中包含的憑證服務備份金鑰 \# 可以由 [憑證授權單位單位] mmc 嵌入式管理單元來還原，或是由 certutil 命令 (指定-restore 或-restorekey 動詞) 來還原，請注意執行還原作業的人員必須知道 PKCS 12 檔案的密碼 \# 。</span><span class="sxs-lookup"><span data-stu-id="c5c4d-110">A Certificate Services backup key contained in a PKCS \#12 file can be restored by the Certification Authority MMC snap-in, or by the certutil command (specifying the -restore or -restorekey verbs); note that the person performing the restore operation will need to know the password for the PKCS \#12 file.</span></span>

<span data-ttu-id="c5c4d-111">只有兩種情況下必須備份憑證服務私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5c4d-111">There are only two cases in which a Certificate Services private key must be backed up.</span></span> <span data-ttu-id="c5c4d-112">第一個案例是在安裝憑證服務之後。</span><span class="sxs-lookup"><span data-stu-id="c5c4d-112">The first case is after the installation of Certificate Services.</span></span> <span data-ttu-id="c5c4d-113">第二個案例是在憑證服務憑證的任何更新作業之後。</span><span class="sxs-lookup"><span data-stu-id="c5c4d-113">The second case is after any renewal operation of the Certificate Services certificate.</span></span>

 

 
