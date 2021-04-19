---
title: 金鑰和金鑰識別碼
description: 金鑰和金鑰識別碼
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- 數位版權管理 (DRM) ，金鑰
- DRM (數位版權管理) 、金鑰
- 數位版權管理 (DRM) ，小孩
- DRM (數位版權管理) ，小孩
- '金鑰識別碼 (小孩) '
- '小孩 (金鑰識別碼) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967820"
---
# <a name="key-and-key-id"></a>金鑰和金鑰識別碼

當您封裝檔案時，您會使用金鑰。 金鑰是用於保護內容的加密演算法中所使用的一段資料。 每個金鑰都有兩個部分：授權金鑰植入和金鑰識別碼， (通常縮寫為小孩) 。 金鑰識別碼是公用的，而且會儲存在檔案標頭中，以識別解密檔案所需的金鑰。 授權金鑰種子是內容封裝程式和授權簽發者必須共用的秘密值。

金鑰識別碼會從授權的觀點來識別受保護的內容。 雖然您可以將相同的金鑰識別碼用於多個檔案，但建議您一律針對每個受保護的內容使用唯一的金鑰識別碼。

本檔中所述的許多方法都使用金鑰識別碼字串來選取授權。 這些字串包含以 base64 編碼的金鑰識別碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**概念**](drmconcepts.md)
</dt> </dl>

 

 




