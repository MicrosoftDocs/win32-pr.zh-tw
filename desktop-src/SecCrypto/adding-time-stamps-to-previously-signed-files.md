---
description: 當使用 SignTool 搭配-t 選項簽署檔案時，通常會包含時間戳記。
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: 將時間戳記新增至先前簽署的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988f63e7b5c58f5d8346d074d3ec98d31dc87443670480f7ded2e72f2272275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880228"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>將時間戳記新增至先前簽署的檔案

當使用 SignTool 搭配 **-t** 選項簽署檔案時，通常會包含時間戳記。 此外，您可以將時間戳記新增至未經過時間戳記簽署的檔案。 下列命令會將時間戳記新增至先前簽署的檔案：

**signtool timestamp-t HTTPs： \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> 要加上時間戳記的檔案必須先前已簽署。

 

如需 SignTool 的詳細資訊，請參閱 [SignTool](signtool.md)。

 

 



