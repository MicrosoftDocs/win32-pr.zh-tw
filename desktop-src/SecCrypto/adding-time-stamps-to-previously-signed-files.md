---
description: 當使用 SignTool 搭配-t 選項簽署檔案時，通常會包含時間戳記。
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: 將時間戳記新增至先前簽署的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106999965"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>將時間戳記新增至先前簽署的檔案

當使用 SignTool 搭配 **-t** 選項簽署檔案時，通常會包含時間戳記。 此外，您可以將時間戳記新增至未經過時間戳記簽署的檔案。 下列命令會將時間戳記新增至先前簽署的檔案：

**signtool timestamp-t HTTPs： \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> 要加上時間戳記的檔案必須先前已簽署。

 

如需 SignTool 的詳細資訊，請參閱 [SignTool](signtool.md)。

 

 



