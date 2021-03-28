---
description: 示範如何註冊可延伸 &0034 的動詞 \# ;同步&\# 0034; 和 &\# 0034; \#在 Windows 檔案總管命令列中共用&0034; 動詞。
title: 同步和共用動詞
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973748"
---
# <a name="sync-and-share-verbs"></a>同步和共用動詞

示範如何註冊在 Windows 檔案總管命令列中擴充「同步處理」和「共用」動詞命令的動詞。

本主題包含下列各節。

-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [執行範例](#running-the-sample)
-   [移除範例](#removing-the-sample)

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [SyncAndShareVerbs 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a>執行範例

若要執行範例 (同步) ：

1.  流覽至 `sync.reg` 包含該檔案的目錄
2.  `sync.reg `在命令列中輸入，或按兩下圖示進行 `sync.reg` 註冊。
3.  開啟 Windows 檔案總管，然後選取檔案。
4.  按一下命令列中的 [ **同步** 處理] 選項，然後選取子選項，例如 [ **繪製**]。

若要執行範例 (共用) ：

1.  流覽至包含該檔案的目錄 `share.reg` 。
2.  `share.reg`在命令列中輸入，或按兩下圖示進行 `share.reg` 註冊。
3.  開啟 Windows 檔案總管然後選取檔案。 按一下命令列中的 [ **共用** ] 選項。
4.  按一下命令列中的 [ **共用方式** ] 選項，然後選取子選項，例如 [ **繪製**]。

## <a name="removing-the-sample"></a>移除範例

若要移除範例 (同步) ：

1.  流覽至包含 Uninstallsync .reg 檔案的目錄。
2.  `uninstallsync.reg`在命令列中輸入，或按兩下的圖示 `uninstallsync.reg` 。

若要移除範例 (共用) ：

1.  流覽至包含 Uninstallshare .reg 檔案的目錄。
2.  `uninstallshare.reg`在命令列中輸入，或按兩下圖示`uninstallshare.reg.`

 

 



