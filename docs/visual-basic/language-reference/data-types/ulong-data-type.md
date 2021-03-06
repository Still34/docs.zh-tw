---
title: ULong 資料類型 (Visual Basic)
ms.date: 01/31/2018
f1_keywords:
- vb.ulong
helpviewer_keywords:
- numbers [Visual Basic], whole
- whole numbers
- integral data types [Visual Basic]
- integer numbers
- numbers [Visual Basic], integer
- integers [Visual Basic], data types
- integers [Visual Basic], types
- data types [Visual Basic], integral
- literal type characters [Visual Basic], UL
- ULong data type
- UL literal type characters [Visual Basic]
ms.assetid: 017e0702-774e-44ae-bedc-786b424ca84e
ms.openlocfilehash: 13dec9f298655a4bfe6672e2dbba7c7262379cc4
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2018
ms.locfileid: "50033528"
---
# <a name="ulong-data-type-visual-basic"></a>ULong 資料類型 (Visual Basic)

保存不帶正負號的 64 位元 （8 個位元組） 整數值範圍從 0 到 18446744073709551615 (超過 1.84 乘以 10 ^19)。  
  
## <a name="remarks"></a>備註

使用`ULong`資料類型可包含二進位資料太大， `UInteger`，或最大可能的不帶正負號的整數值。  
  
`ULong` 的預設值為 0。

## <a name="literal-assignments"></a>常值的指派

您可以宣告並初始化`ULong`變數指派十進位常值、 十六進位常值、 八進位的常值，或 （Visual Basic 2017 年起） 二進位常值。 如果整數常值超出 `ULong` 的範圍 (亦即，如果小於 <xref:System.UInt64.MinValue?displayProperty=nameWithType> 或大於 <xref:System.UInt64.MaxValue?displayProperty=nameWithType>)，就會發生編譯錯誤。

在下列範例中，以十進位、十六進位和二進位常值表示的 7,934,076,125 整數，會指派給 `ULong` 值。
  
[!code-vb[ULong](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#ULong)]

> [!NOTE] 
> 使用前置詞`&h`或是`&H`來表示十六進位常值前置詞`&b`或`&B`代表二進位常值，以及前置詞`&o`或`&O`代表八進位的常值。 十進位常值沒有前置詞。

從 Visual Basic 2017 開始，您也可以使用底線字元`_`，作為數字分隔符號，以提升可讀性，如下列範例所示。

[!code-vb[ULong](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#LongS)]

從 Visual Basic 15.5 開始，您也可以使用底線字元 (`_`) 作為前置分隔符號之間的前置詞和十六進位、 二進位或八進位數字。 例如: 

```vb
Dim number As ULong = &H_F9AC_0326_1489_D68C
```

[!INCLUDE [supporting-underscores](../../../../includes/vb-separator-langversion.md)]

也可以包含數值常值`UL`或是`ul`[型別字元](../../programming-guide\language-features\data-types/type-characters.md)表示`ULong`資料型別，如下列範例所示。

```vb
Dim number = &H_00_00_0A_96_2F_AC_14_D7ul
```

## <a name="programming-tips"></a>程式設計提示
  
-   **負數的數字。** 因為`ULong`是不帶正負號的型別，它無法表示負數。 如果您使用一元減號 (`-`) 運算子的運算式，評估為類型`ULong`，Visual Basic 會將轉換的運算式`Decimal`第一次。  
  
-   **CLS 合規性。** `ULong`資料類型不是屬於[Common Language Specification](http://www.ecma-international.org/publications/standards/Ecma-335.htm) （cls） 標準，所以符合 CLS 標準的程式碼無法取用使用它的元件。  
  
-   **Interop 考量。** 如果您要使用的元件不是撰寫.NET framework，例如 Automation 或 COM 物件，請記住，這類類型`ulong`在其他環境中可以有不同的資料寬度 （32 位元）。 如果您在這類元件傳遞 32 位元引數，將它宣告為`UInteger`而不是`ULong`中受管理的 Visual Basic 程式碼。  
  
     此外，自動化不支援在 Windows 95、 Windows 98、 Windows ME，或 Windows 2000 64 位元整數。 您不能傳遞 Visual Basic`ULong`自動化元件，這些平台上的引數。  
  
-   **擴展。** `ULong`資料類型可擴展為`Decimal`， `Single`，和`Double`。 這表示您可以將轉換`ULong`任何一種類型，而不會發生<xref:System.OverflowException?displayProperty=nameWithType>時發生錯誤。  
  
-   **類型字元。** 將常值類型字元附加`UL`成常值會強制其成為`ULong`資料型別。 `ULong` 有任何識別項類型字元。
  
-   **Framework 型別。** 在 .NET Framework 中對應的類型為 <xref:System.UInt64?displayProperty=nameWithType> 結構。  
  
## <a name="see-also"></a>另請參閱

 <xref:System.UInt64>  
 [資料類型](../../../visual-basic/language-reference/data-types/index.md)  
 [類型轉換函式](../../../visual-basic/language-reference/functions/type-conversion-functions.md)  
 [轉換摘要](../../../visual-basic/language-reference/keywords/conversion-summary.md)  
 [操作說明：呼叫使用不帶正負號類型的 Windows 函式](../../../visual-basic/programming-guide/com-interop/how-to-call-a-windows-function-that-takes-unsigned-types.md)  
 [有效率地使用資料類型](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
