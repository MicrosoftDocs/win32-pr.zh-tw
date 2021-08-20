---
description: 稀疏檔案會依檔案的名義大小來影響使用者配額，而不是實際配置的磁碟空間量。
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: 稀疏檔案和磁片配額
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e78e9d35e557585f17df6c4672a04b2997792f95b0fca63d2e6a2345a7a8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015076"
---
# <a name="sparse-files-and-disk-quotas"></a>稀疏檔案和磁片配額

稀疏檔案會依檔案的名義大小來影響使用者配額，而不是實際配置的磁碟空間量。 也就是說，若要建立具有零個位元組的 50 MB 檔案，就會耗用該使用者配額的 50 MB。 這表示當使用者將資料寫入至稀疏檔案時，他不需要擔心超過其硬性配額限制，因為該空間已收取空間的費用。 系統管理員不應計算較小的稀疏檔案大小。 因此，不論使用的是稀疏檔案，它們都不應將超過可用實體空間的硬性配額限制授與使用者。

 

 



