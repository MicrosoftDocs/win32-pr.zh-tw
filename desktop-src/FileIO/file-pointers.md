---
description: 檔案指標是64位的位移值，可指定要讀取的下一個位元組，或要接收下一個寫入位元組的位置。
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: 檔案指標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192124"
---
# <a name="file-pointers"></a>檔案指標

開啟檔案時，Windows 會將檔案 *指標* 與預設資料流程產生關聯。 這個檔案指標是64位的位移值，可指定要讀取的下一個位元組，或要接收下一個寫入位元組的位置。 每次開啟檔案時，系統會將檔案指標放在檔案的開頭，也就是位移零。 每個讀取和寫入作業都會依所讀取和寫入的位元組數目來推進檔案指標。 例如，如果檔案指標位於檔案的開頭，且要求了5個位元組的讀取作業，則檔案指標會緊接在讀取作業之後的位移5。 當讀取或寫入每個位元組時，系統會將檔案指標前進。 藉由呼叫 [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) 函式，也可以重新置放檔案指標。

當檔案指標到達檔案結尾，而應用程式嘗試從檔案讀取時，不會發生任何錯誤，但不會讀取任何位元組。 因此，讀取零位元組而不發生錯誤，表示應用程式已到達檔案結尾。 寫入零位元組不會執行任何動作。

應用程式可以使用 [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) 函數來截斷或擴充檔案。 此函式會將檔案結尾設定為檔案指標的目前位置。

 

 



