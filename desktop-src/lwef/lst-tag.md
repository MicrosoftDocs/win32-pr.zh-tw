---
title: .Lst 標記
description: .Lst 標記
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad70173ef3919ae2291204745f727961165a83f4f0fad0ad310003b997a5565e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114588"
---
# <a name="lst-tag"></a>.Lst 標記

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

針對字元重複最後一個讀出的語句。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

\\**Lst**\\

</dd> </dl>

### <a name="remarks"></a>備註

此標記可讓字元重複其最後一個讀出的語句。 這個標記必須單獨出現在 [**說話**](speak-method.md) 方法中;不能包含任何其他文字或參數。 當說出文字重複時，原始文字中包含的任何其他標記都會重複，除了書簽以外。 任何。WAV 和。文字中包含的 LWV 檔也會重複。

 

 




