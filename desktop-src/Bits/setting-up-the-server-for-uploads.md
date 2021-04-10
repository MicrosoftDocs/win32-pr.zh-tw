---
title: 設定伺服器以進行上傳
description: 若要使用 BITS 將檔案上傳到伺服器，伺服器必須已安裝 IIS 和 BITS 伺服器延伸 ISAPI。 如需 IIS 需求，請參閱 IIS 的 BITS 上傳需求。
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183045"
---
# <a name="setting-up-the-server-for-uploads"></a>設定伺服器以進行上傳

若要使用 BITS 將檔案上傳到伺服器，伺服器必須已安裝 IIS 和 BITS 伺服器延伸 ISAPI。 如需 IIS 需求，請參閱 [iis 的 BITS 上傳需求](iis-requirements-for-bits-uploads.md)。

如需設定 BITS 用於上傳之 IIS 虛擬目錄的詳細資訊，請參閱下列主題。

-   [設定虛擬目錄的許可權](setting-permissions-on-virtual-directories.md)
-   [撰寫腳本來設定虛擬目錄](writing-a-script-to-configure-the-virtual-directory.md)
-   [使用 IIS UI 來設定虛擬目錄](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [防止多個上傳](preventing-multiple-uploads.md)
-   [上傳最佳作法](upload-best-practices.md)

> [!Note]  
> 部分 IIS 安裝包含 UrlScan 篩選元件。 如果已啟用 UrlScan，則系統管理員必須將 "BITS \_ POST" 動詞新增至 UrlScan 的允許 HTTP 動詞命令清單。 否則，BITS 用戶端上傳將會失敗。 如需在 UrlScan 中啟用動詞的詳細資訊，請參閱 UrlScan 檔。

 

 

 




