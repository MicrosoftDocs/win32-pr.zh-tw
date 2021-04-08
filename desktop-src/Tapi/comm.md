---
description: 通訊裝置類別包含通訊埠。 您可以使用檔案和通訊功能來存取這些裝置。
ms.assetid: c1cf4998-b752-4cfd-9dd7-c9872b62c44b
title: 通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40136654d7e308f30e4e27467cf5e21385340841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691176"
---
# <a name="comm"></a>通訊

通訊裝置類別包含通訊埠。 您可以使用[檔案和](/windows/desktop/FileIO/file-management-functions)[通訊功能](/windows/desktop/DevIO/communications-functions)來存取這些裝置。

[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構、將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ ASCII 值，並附加以 null 終止的字串，以指定通訊裝置的名稱 (例如數據機名稱) 。

 

 
