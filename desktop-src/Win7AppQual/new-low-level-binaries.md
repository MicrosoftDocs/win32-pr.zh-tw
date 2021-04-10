---
description: .
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: 新的 Low-Level 二進位檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b6e197f22df9fb3d6e12aeeff3c5f4a2a0e41c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194156"
---
# <a name="new-low-level-binaries"></a>新的 Low-Level 二進位檔

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows 7  
**伺服器** -Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

**嚴重性** -中  
**頻率** -高  











## <a name="description"></a>Description

為了改善內部工程效率並改善未來工作的基礎，我們已將一些功能重新放置到新的低層級二進位檔。 這項重整功能可讓您在未來的 Windows 安裝中提供功能子集，以縮減介面區 (磁片和記憶體需求、服務以及受攻擊面) 。

## <a name="manifestation-of-impact"></a>影響的表現

作為我們移至低層級二進位檔的功能範例，kernelbase.dll 從 kernel32.dll 和 advapi32.dll 取得功能。 這表示現有的二進位檔現在會將呼叫向下轉送至新的二進位檔，而不是直接處理它們;轉送可以是靜態 (匯出資料表會顯示重新導向) ， (或 dll 具有可向下呼叫新二進位) 的存根常式。 這會影響低層級的應用程式，例如與內部 Api 和位移相依的安全性和備份應用程式。

## <a name="solution"></a>解決方法

唯一的影響是嘗試查看 kernel32.dll 的程式碼，或在記憶體中 advapi32.dll 匯出資料表的程式碼，例如防毒程式可能會執行的動作。 使用已發佈的 Api，而不是其執行的詳細資料。 這只是執行 API 的詳細資料的一個範例。

 

 



