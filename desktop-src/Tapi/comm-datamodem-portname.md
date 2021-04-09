---
description: Comm/datamodem/portname 裝置類別是由數據機所連接的裝置名稱所組成。
ms.assetid: 174519f6-3e73-4f05-9718-9e38680a0fb7
title: 通訊/datamodem/portname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f926dc87a093f49d41256b003e47c048caa5ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850804"
---
# <a name="commdatamodemportname"></a>通訊/datamodem/portname

Comm/datamodem/portname 裝置類別是由數據機所連接的裝置名稱所組成。 在對 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) 函式的呼叫中指定這個裝置名稱時，函式會以以 null 終止的 ANSI (非 Unicode) 字串來填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) 結構，指定連接指定數據機的埠名稱，例如 "COM1 \\ 0"。 這主要是為了在使用者介面中進行識別，但在某些情況下，如果服務提供者尚未讓裝置開啟) ，就可以在某些情況下用來直接開啟裝置，略過服務提供者的 (。 如果沒有與裝置相關聯的通訊埠，就 \\ 會在 **VARSTRING** 結構中傳回 null 字串 ( "0" )  (字串長度為 1) 。

 

 



