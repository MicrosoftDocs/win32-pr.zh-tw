---
description: 如果在檔案 \_ 複製作業期間指定了 SP 複製 \_ 較新的旗標，則安裝程式會檢查目標目錄中是否有檔案的現有複本。
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: 檔案版本比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9601dcef07afca81a3ffc64148b0c4f2492f935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985285"
---
# <a name="file-version-comparisons"></a>檔案版本比較

如果在檔案 \_ 複製作業期間指定了 SP 複製 \_ 較新的旗標，則安裝程式會檢查目標目錄中是否有檔案的現有複本。 如果找到現有的複本，這些函式會比較目標和來源檔案的版本，以判斷哪一個是較新的版本。

版本檢查期間使用的檔案版本資訊，是在版本函式所使用之 [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)結構的 **dwFileVersionMS** 和 **dwFileVersionLS** 成員中指定的。 如果其中一個檔案未指定版本資源，或有相同的版本資訊，則會將原始程式檔視為較新的檔案。

 

 
