---
title: 執行記憶體檔 i/o
description: 執行記憶體檔 i/o
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- 多媒體檔案 i/o，記憶體
- 檔案 i/o，記憶體
- 輸入和輸出 (i/o) ，記憶體
- I/o (輸入和輸出) ，記憶體
- 記憶體 i/o
- mmioOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462961"
---
# <a name="performing-memory-file-io"></a>執行記憶體檔 i/o

多媒體檔案 i/o 服務可讓您將記憶體區塊視為檔案。 如果您在記憶體中已經有檔案映射，這會很有用。 記憶體檔案可讓您減少程式碼中的特殊案例數目，因為基於 i/o 用途，您可以將記憶體檔案視為磁片型檔案。 您也可以使用記憶體檔案搭配剪貼簿。

就像 i/o 緩衝區一樣，記憶體檔案也可以使用應用程式所配置的記憶體或檔案 i/o 管理員所配置的記憶體。 此外，記憶體檔案可以是可擴充或 nonexpandable。 當檔案 i/o 管理員到達可延伸記憶體檔案的結尾時，它會依預先定義的增量展開記憶體檔案。

若要開啟記憶體檔案，請使用 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 函數，並將 *szFilename* 參數設定為 **Null** ，並 \_ 在 *dwOpenFlags* 參數中設定 MMIO READWRITE 旗標。 將 *lpmmioinfo* 參數設定為指向已設定的 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) 結構，如下所示：

1.  將 **pIOProc** 成員設定為 **Null**。
2.  將 **fccIOProc** 成員設定為 FOURCC \_ MEM。
3.  設定 **pchBuffer** 成員以指向記憶體區塊。 若要要求檔案 i/o 管理員配置記憶體區塊，請將 **pchBuffer** 設定為 **Null**。
4.  將 **cchBuffer** 成員設定為記憶體區塊的初始大小。
5.  將 **adwInfo** 成員設定為記憶體區塊的最小擴充大小。 若為 nonexpandable 記憶體檔案，請將 **adwInfo** 設定為 **Null**。
6.  將所有其他成員設定為零。

配置記憶體以做為 nonexpandable 記憶體檔案沒有任何限制。

 

 