---
description: '[磁碟空間] 清單可讓您計算完成安裝作業所需的磁碟空間。'
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: 關於 Disk-Space 清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b092d73c00f426fe5c0ab298e4b6a53c19131c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973040"
---
# <a name="about-the-disk-space-list"></a><span data-ttu-id="7e2a8-103">關於 Disk-Space 清單</span><span class="sxs-lookup"><span data-stu-id="7e2a8-103">About the Disk-Space List</span></span>

<span data-ttu-id="7e2a8-104">[磁碟空間] 清單可讓您計算完成安裝作業所需的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="7e2a8-104">The disk-space list enables you to calculate the disk space required to complete the installation operations.</span></span> <span data-ttu-id="7e2a8-105">建立磁碟空間清單並在其中新增檔案作業之後，您可以查詢清單，以判斷檔案操作所指定的目標磁片磁碟機，以及每個磁片磁碟機上所需的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="7e2a8-105">After you create a disk-space list and add file operations to it, you can query the list to determine the target drives specified by the file operations, and the disk space required on each drive.</span></span>

<span data-ttu-id="7e2a8-106">藉由比較目標磁片上可用空間的空間，您可以用程式設計的方式判斷是否有足夠的空間可用於目前的安裝。</span><span class="sxs-lookup"><span data-stu-id="7e2a8-106">By comparing the space required to the space available on the target disks, you can programmatically determine whether sufficient space is available for the current installation.</span></span>

<span data-ttu-id="7e2a8-107">您可以新增或移除磁碟空間清單中的檔案作業，並重新計算所需的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="7e2a8-107">You can add or remove file operations to the disk-space list and recalculate the disk space required.</span></span> <span data-ttu-id="7e2a8-108">例如，此功能可讓您撰寫與使用者互動的程式，讓他或她根據所需的磁碟空間，選擇要安裝的元件。</span><span class="sxs-lookup"><span data-stu-id="7e2a8-108">This functionality enables you to, for example, write a program that interacts with the user, allowing him or her to choose what components they want to install based on the disk space required.</span></span>

<span data-ttu-id="7e2a8-109">磁碟空間清單功能會自動檢查目標磁片上是否有預先存在的檔案複本。</span><span class="sxs-lookup"><span data-stu-id="7e2a8-109">The disk-space list functions automatically check for preexisting copies of files on the target disk.</span></span> <span data-ttu-id="7e2a8-110">如果找到舊版本的檔案，則磁碟空間清單函式會計算完成檔案作業所需的額外空間。</span><span class="sxs-lookup"><span data-stu-id="7e2a8-110">If a previous version of the file is found, the disk-space list functions calculate the additional space required to complete the file operations.</span></span>

<span data-ttu-id="7e2a8-111">例如，如果複製作業指定將6000位元組檔案複製到 C 磁片磁碟機，而磁片磁碟機 C 上已經有2000位元組版本的檔案，則磁碟空間函數會傳回所需的4000位元組空間。</span><span class="sxs-lookup"><span data-stu-id="7e2a8-111">For example, if a copy operation specifies that a 6000-byte file be copied to drive C, and a 2000-byte version of that file already exists on the drive C, the disk space functions would return a required space of 4000 bytes.</span></span> <span data-ttu-id="7e2a8-112">額外的空間是用來以較新的版本取代較舊版本的檔案。</span><span class="sxs-lookup"><span data-stu-id="7e2a8-112">The additional space is used to replace the older version of the file with the newer version.</span></span>

<span data-ttu-id="7e2a8-113">磁碟空間清單會將檔案大小四捨五入到磁片叢集界限。</span><span class="sxs-lookup"><span data-stu-id="7e2a8-113">The disk-space list functions round file sizes to the disk cluster boundaries.</span></span>

 

 



