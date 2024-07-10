# Tarea-de-alejandra
Casa en idioms vrml de codigo abierto

      translation 0 -1 0
      children [
        Shape {
          appearance Appearance {
            texture ImageTexture {
              url "suelo.jpg"  # Añadir la textura del suelo
            }
          }
          geometry IndexedFaceSet {
            coord Coordinate {
              point [
                -50 0 -50,  50 0 -50,  50 0 50,  -50 0 50
              ]
            }
            coordIndex [
              0 1 2 -1,
              0 2 3 -1
            ]
          }
        }
      ]
    }

    # Definición del cielo (fondo)
    Transform {
      translation 0 20 -50  # Posición ajustable según la escala del paisaje
      children [
        Shape {
          appearance Appearance {
            texture ImageTexture {
              url "cielo.jpg"  # Añadir la textura del cielo
            }
          }
          geometry Box {
            size 200 0.1 100  # Ajustar el tamaño según el paisaje
          }
        }
      ]
    }

    # Definición de la casa
    Transform {
      translation 0 0 0
      children [
        Group {  # Grupo para la estructura de la casa
          children [
            # Paredes de la casa
            Transform {
              translation 0 2.5 0
              children [
                Shape {
                  appearance Appearance {
                    material Material {
                      diffuseColor 0.8 0.8 0.8
                    }
                  }
                  geometry Box {
                    size 10 5 8
                  }
                }
              ]
            }

            # Techo de la casa
            Transform {
              translation 0 5.5 0
              children [
                Shape {
                  appearance Appearance {
                    material Material {
                      diffuseColor 0.5 0.1 0.1
                    }
                  }
                  geometry Cone {
                    bottomRadius 5
                    height 3
                  }
                }
              ]
            }

            # Puerta de la casa
            Transform {
              translation 0 1.5 4.01
              children [
                Shape {
                  appearance Appearance {
                    material Material {
                      diffuseColor 0.2 0.1 0.6
                    }
                  }
                  geometry Box {
                    size 2.5 3 0.1
                  }
                }
              ]
            }

            # Ventanas de la casa
            Transform {
              translation -3 3 2.51
              children [
                Shape {
                  appearance Appearance {
                    material Material {
                      diffuseColor 0.6 0.8 1
                    }
                  }
                  geometry Box {
                    size 1 2 0.1
                  }
                }
              ]
            }

            Transform {
              translation 3 3 2.51
              children [
                Shape {
                  appearance Appearance {
                    material Material {
                      diffuseColor 0.6 0.8 1
                    }
                  }
                  geometry Box {
                    size 1 2 0.1
                  }
                }
              ]
            }
          ]
        }
      ]
    }

    # Otros elementos del paisaje (árboles, caminos, etc.)
    Transform {
      translation -10 0 -10
      children [
        Shape {
          appearance Appearance {
            material Material {
              diffuseColor 0.3 0.5 0.2
            }
          }
          geometry Cylinder {
            radius 0.5
            height 5
          }
        }
      ]
    }

    Transform {
      translation 10 0 -10
      children [
        Shape {
          appearance Appearance {
            material Material {
              diffuseColor 0.3 0.5 0.2
            }
          }
          geometry Cylinder {
            radius 0.5
            height 5
          }
        }
      ]
    }
  ]
}

